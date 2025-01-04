# 递归合并文件夹中的markdown文件



如何使用merge_markdown使用，请阅读我



1、前置，安装python，安装成功后检查版本

```bash
Microsoft Windows [版本 10.0.19045.5247]
(c) Microsoft Corporation。保留所有权利。

C:\Users\mfc>python --version
Python 3.10.0

C:\Users\mfc>


```



2、创建`merge_markdown.py`文件

```python 
import os
from pathlib import Path
import argparse
import re

def validate_directory(directory):
    """验证目录是否存在并包含 Markdown 文件"""
    if not os.path.isdir(directory):
        print(f"Error: The directory '{directory}' does not exist.")
        return False
    md_files = [f for f in os.listdir(directory) if f.lower().endswith('.md')]
    if not md_files:
        print(f"Warning: No Markdown files found in '{directory}'.")
    else:
        print(f"Found {len(md_files)} Markdown file(s) in '{directory}'.")
    return True

def ensure_output_directory(output_file_path):
    """确保输出文件的目录存在，如果不存在则创建"""
    output_dir = os.path.dirname(os.path.abspath(output_file_path))
    if not os.path.exists(output_dir):
        print(f"Creating output directory: {output_dir}")
        os.makedirs(output_dir)


def convert_paths_to_absolute(content, root_dir, base_dir):
    """将 Markdown 文件中的图片引用和普通链接的相对路径转换为绝对路径"""
    
    def replace_path(match):
        # 获取括号中的路径部分
        img_or_link_path = match.group(2)
        print(f"Found path: {img_or_link_path}")  # 打印路径部分，用于调试
        
        # 只替换包含 'images/' 的路径
        if 'images/' in img_or_link_path:
            abs_path = os.path.join(base_dir, img_or_link_path).replace('\\', '/')
            print(f"Converting path: {img_or_link_path} -> {abs_path}")  # 打印调试信息
            return abs_path
        return img_or_link_path  # 如果不包含 'images/'，返回原路径

    # 正则表达式匹配 Markdown 图片引用格式: ![alt text](image_path)
    image_pattern = re.compile(r'!\[([^\]]*)\]\(([^)]+)\)')  # 修正正则，确保正确匹配
    content = image_pattern.sub(lambda m: f"![{m.group(1)}]({replace_path(m)})", content)

    return content


def merge_markdown_files(directory, output_file_path, ignore_dirs=None, ignore_files=None):
    if ignore_dirs is None:
        ignore_dirs = {'.git','images'}  # 默认忽略 .git 文件夹
    if ignore_files is None:
        ignore_files = {'README.md'}  # 默认忽略 README.md 文件
    
    processed_files = set()  # 用于跟踪已经处理过的文件的绝对路径
    
    # 确保输出文件的目录存在
    ensure_output_directory(output_file_path)

    # 获取输出文件的绝对路径并打印调试信息
    abs_output_path = os.path.abspath(output_file_path)
    print(f"Output file will be saved to: {abs_output_path}")

    with open(output_file_path, 'w', encoding='utf-8') as outfile:
        for root, dirs, files in os.walk(directory):
            # 修改 dirs 列表以排除不需要处理的子目录
            dirs[:] = [d for d in dirs if d not in ignore_dirs]

            # 获取相对路径以用作标题
            relative_path = Path(root).relative_to(directory)
            if relative_path != Path('.'):
                outfile.write(f'# {relative_path}\n\n')

            # 对每个文件进行排序（按字母顺序），然后合并内容
            md_files = sorted([f for f in files if f.lower().endswith('.md') and f.lower() not in ignore_files])
            if not md_files:
                print(f"No Markdown files found in '{root}'.")
                continue

            for file in md_files:
                filepath = os.path.join(root, file)
                abs_filepath = os.path.abspath(filepath)  # 获取文件的绝对路径
                if abs_filepath not in processed_files:  # 检查是否已经处理过该文件
                    print(f"Processing file: {abs_filepath}")  # 打印调试信息
                    with open(filepath, 'r', encoding='utf-8') as infile:
                        content = infile.read()
                        # 将图片引用和普通链接的路径转换为绝对路径
                        content = convert_paths_to_absolute(content, directory, root)
                        outfile.write(content)
                        outfile.write('\n\n---\n\n')  # 分隔符
                    processed_files.add(abs_filepath)  # 将文件的绝对路径添加到已处理列表中
                else:
                    print(f"Skipping duplicate file: {abs_filepath}")  # 打印调试信息

if __name__ == "__main__":
    # 设置命令行参数解析器
    parser = argparse.ArgumentParser(description="Merge all Markdown files in a directory into one.")
    
    # 添加命令行参数
    parser.add_argument('directory', help='The directory containing the Markdown files to be merged.')
    parser.add_argument('output_file', help='The output file where the merged content will be saved. Can be an absolute or relative path.')

    # 解析命令行参数
    args = parser.parse_args()

    # 验证输入目录
    if not validate_directory(args.directory):
        exit(1)

    # 使用解析后的参数调用函数
    merge_markdown_files(args.directory, args.output_file)
```





3、使用`merge_markdown.py`，cmd：

```bash
D:

cd D:\repository\github\CloudNative

python merge_markdown.py "D:/repository/github/CloudNative" "D:/output/combined.md"
```

