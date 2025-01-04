# 使用pandoc创建pdf



> 这个pandoc是完全自定义pdf的效果的，可以借助LaTeX实现自己想要的各种效果，给向折腾的同学使用。
>
> 当然，图方便的话可以直接使用typora导出pdf。



1、安装 Pandoc 和 LaTeX（TeX Live）后，检查版本

pandoc

```bash
C:\Users\mfc>pandoc --version
pandoc 3.6.1
Features: +server +lua
Scripting engine: Lua 5.4
User data directory: C:\Users\mfc\AppData\Roaming\pandoc
Copyright (C) 2006-2024 John MacFarlane. Web: https://pandoc.org
This is free software; see the source for copying conditions. There is no
warranty, not even for merchantability or fitness for a particular purpose.

C:\Users\mfc>
```

TeX Live

```bash
C:\Users\mfc>tex --version
TeX 3.141592653 (TeX Live 2024)
kpathsea version 6.4.0
Copyright 2024 D.E. Knuth.
There is NO warranty.  Redistribution of this software is
covered by the terms of both the TeX copyright and
the Lesser GNU General Public License.
For more information about these matters, see the file
named COPYING and the TeX source.
Primary author of TeX: D.E. Knuth.

C:\Users\mfc>
```



2、定义preamble.tex，实现各种pdf效果

```latex
% 中文支持
\usepackage{xeCJK}                   
\setCJKmainfont{SimSun}             % 主字体为宋体
\setCJKsansfont{SimHei}             % 无衬线字体为黑体
\setCJKmonofont{FangSong}           % 等宽字体为仿宋

% 页面布局
\usepackage{geometry}                
\geometry{a4paper, margin=1in}      % 设置页面边距

% 超链接支持
\usepackage{hyperref}
\hypersetup{
  colorlinks=true,
  linkcolor=blue,                  % 链接文本颜色
  urlcolor=blue                    % URL 地址颜色
}

% 强制图片绝对位置
\usepackage{float}
\let\origfigure\figure
\let\endorigfigure\endfigure
\renewenvironment{figure}[1][]{%
  \origfigure[H]
}{%
  \endorigfigure
}

% 代码块配置
\usepackage{listings}               % 支持代码块
\usepackage{xcolor}                 % 支持颜色
\usepackage{fontspec}               % 支持自定义字体

% 定义颜色
\definecolor{lightgray}{RGB}{240,240,240} % 浅灰色
\definecolor{bordergray}{RGB}{200,200,200} % 边框灰色

% 代码块样式
\lstset{
  backgroundcolor=\color{lightgray},      % 代码块背景色（浅灰色）
  basicstyle=\ttfamily\small,             % 字体设置
  frame=single,                           % 添加边框
  framerule=0.5pt,                        % 边框线宽
  rulecolor=\color{bordergray},           % 边框颜色
  breaklines=true,                        % 自动换行
  showstringspaces=false,                 % 不显示空格标记
  fontadjust=true,                        % 自动调整字体
  keepspaces=true,                        % 保留空格
  basicstyle=\fontspec{DejaVu Sans Mono}, % 设置支持框线字符的字体
  extendedchars=true,                     % 支持扩展字符
  literate={-}{{-}}1                      % 确保 `-` 不被替换
}

% 引用块样式
\usepackage{tcolorbox}             % 支持背景框
\tcbuselibrary{listings, skins}    % 扩展库

% 引用块样式，仅保留左侧边框
\newtcolorbox{quoteBox}{colback=gray!10!white, colframe=gray!50!black, sharp corners, boxrule=0pt, left=5pt, top=0pt, bottom=0pt, borderline west={1pt}{0pt}{gray!50!black}}
\renewenvironment{quote}{\begin{quoteBox}}{\end{quoteBox}}

% 使图片完全没有标签和标题
\usepackage{caption}
\captionsetup{labelformat=empty, labelsep=none} % 完全去掉图片标题和标签
\DeclareCaptionFormat{empty}{} % 设置一个空的标题格式
\captionsetup{format=empty} % 对所有图片使用空的标题格式


```



3、使用pandoc和preamble.tex，生成自定义pdf文档

```bash
D:\output>pandoc combined.md -o output.pdf --pdf-engine=xelatex -V CJKmainfont="SimSun" -H preamble.tex --listings

D:\output>
```



