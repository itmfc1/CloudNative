# CloudNative

> 引言
>
> 自个的笔记输出，随时查看。
>
> 看了就忘，忘了在看。这个都是非常正常的现象，不要太过苛求。
>
> 每个人的记忆能力和学习习惯都是不同的，找到适合自己的方法最重要。
>
> 保持良好的生活习惯，如充足的睡眠、健康的饮食和适量的运动，也对提高记忆力有帮助。
>
> 不要过于苛责自己，适当的压力可以促进学习，但过高的压力反而会适得其反。



云原生

github地址：https://github.com/itmfc1/CloudNative



## 简介



![云原生](images/云原生架构师.png)

## 目录



```bash
├─01-Linux操作系统
│  ├─1-项目部署之-Linux操作系统
│  │  ├─1-Linux概述与安装
│  │  ├─2-Linux基本操作
│  │  └─3-Linux软件安装与配置
│  └─2-Shell编程
│      └─1-Shell编程
├─02-计算机网络基础
│  └─1-计算机网络基础
│      ├─1-前言
│      ├─2-计算机网络概述
│      ├─3-计算机网络体系结构
│      └─4-笔试题讲解
├─03-云原生生态介绍
│  └─1-云原生介绍
│      ├─1-云原生定义
│      ├─2-云原生发展
│      └─3-CNCF云原生全景图
├─04-虚拟化与云计算
│  ├─1-虚拟化技术
│  │  └─1-虚拟化技术介绍
│  └─2-云计算
│      └─1-云计算概念
├─05-容器管理工具Docker
│  ├─1-容器管理工具Docker
│  │  ├─1-应用部署容器化演进之路
│  │  ├─10-Docker容器数据持久化存储机制
│  │  ├─11-Docker容器服务编排利器DockerCompose应用实战
│  │  ├─12-Docker主机集群化方案DockerSwarm
│  │  ├─13-基于Docker容器DevOps应用方案企业业务代码发布系统
│  │  ├─2-容器技术涉及Linux内核关键技术
│  │  ├─3-Docker生态架构及部署
│  │  ├─4-使用容器运行Nginx及docker命令介绍
│  │  ├─5-容器镜像介绍及应用
│  │  ├─6-Docker容器镜像加速器及容器镜像仓库
│  │  ├─7-Docker容器化部署企业级应用集群
│  │  ├─8-Dockerfile精讲及新型容器镜像构建技术
│  │  └─9-Docker容器网络与通信原理深度解析
│  └─2-容器管理工具Docker
│      └─1-容器运行时Docker
├─06-轻量或工业级容器管理工具Containerd
│  └─1-容器管理工具Containerd
│      ├─1-Containerd介绍
│      ├─10-Docker结合Containerd实现容器管理
│      ├─11-Containerd配置使用Harbor容器镜像仓库
│      ├─12-基于nerdctl+buildkit构建容器镜像
│      ├─2-Containerd安装
│      ├─3-Containerd容器镜像管理
│      ├─4-Containerd容器管理
│      ├─5-Containerd使用私有容器镜像仓库Harbor
│      ├─6-ContainerdNamespace管理
│      ├─7-Containerd网络管理
│      ├─8-Containerd容器共享命令空间
│      └─9-Containerd容器数据持久化存储
├─07-Kubernetes应用基础
│  ├─1-Kubernetes集群部署（云原生）
│  │  ├─1-Kubernetes介绍及集群架构
│  │  ├─10-k8s1.26集群使用containerd容器运行时
│  │  ├─11-基于sealos部署高可用Kubernetes集群
│  │  ├─12-k8s1.27集群部署&容器运行时docker
│  │  ├─13-集群部署利器KubeSpray部署k8s1.26版本集群
│  │  ├─2-Kubernetes集群部署方式
│  │  ├─3-使用kubeadm快速部署Kubernetes集群
│  │  ├─4-使用kubeadm快速部署Kubernetes高可用集群
│  │  ├─5-使用RKE部署企业级生产Kubernetes集群
│  │  ├─6-使用二进制方式部署Kubernetes高可用集群(RuntimeDocker)
│  │  ├─7-使用二进制方式部署Kubernetes高可用集群(RuntimeContainerd)
│  │  ├─8-Kubernetes集群UI及主机资源监控
│  │  └─9-kubernetes1.24集群部署
│  ├─10-Kubernetes集群核心概念Service
│  │  ├─1-Service作用
│  │  ├─2-kube-proxy三种代理模式
│  │  ├─3-Service分类及创建
│  │  └─4-SessionAffinity
│  ├─11-安全容器运行时KataContainers
│  │  └─1-安全容器运行时KataContainers
│  ├─12-安全容器运行时gVisor
│  │  └─1-新型沙箱安全容器运行时工具gVisor
│  ├─13-k8s集群应用自动伸缩实践
│  │  ├─1-K8S集群服务水平自动伸缩（HPA）
│  │  ├─2-利用Prometheus自定义指标实现应用水平自动伸缩
│  │  ├─3-K8S集群服务垂直自动伸缩（VPA）
│  │  └─4-基于事件驱动实现K8S应用自动伸缩（KEDA）
│  ├─14-全链路灰度发布解决方案
│  │  ├─1-使用Argo-Rollouts实现金丝雀发布
│  │  ├─2-原地升级解决方案OpenKruise
│  │  └─3-全链路灰度发布解决方案KruiseRollouts
│  ├─2-Kubernetes集群部署（云原生）
│  │  ├─1-基于cri-o部署K8S1.27版本集群
│  │  ├─10-注重K8S安全RKE2部署K8S高可用集群
│  │  ├─11-RockyLinux操作系统部署K8S集群
│  │  ├─12-信创国产操作系统OpenEuler部署K8S集群
│  │  ├─13-信创国产麒麟(KylinOS)操作系统部署K8S集群
│  │  ├─14-OpenEuler22.03基于iSulad部署K8S集群
│  │  ├─15-kubernetes集群部署口袋工具minikube
│  │  ├─16-kube-vip实现K8S集群高可用及ServiceLB
│  │  ├─17-使用kubeadm快速部署K8S1.29.0集群
│  │  ├─18-使用k0s部署K8S二进制集群
│  │  ├─19-基于Ubuntu22.04部署原生K8S1.29.0集群
│  │  ├─2-使用kubeasz部署k8s二进制高可用集群
│  │  ├─3-基于Containerd部署K8S1.28版本集群
│  │  ├─4-基于Docker部署K8S1.28版本集群
│  │  ├─5-K8S二进制高可用集群部署（多容器运行时）
│  │  ├─6-构建网络高性能（Cilium）K8S集群
│  │  ├─7-基于Ubuntu22.04操作系统部署K8S集群
│  │  ├─8-基于Ubuntu23.04操作系统部署K8S集群
│  │  └─9-Debian12部署K8S最佳实践
│  ├─3-Kubernetes集群客户端命令kubectl
│  │  └─1-Kubernetes集群客户端工具kubectl
│  ├─4-Kubernetes集群Node管理
│  │  └─1-Kubernetes集群Node管理
│  ├─5-Kubernetes集群声明式文件YAML
│  │  └─1-Kubernetes集群声明式文件YAML
│  ├─6-kubernetes集群Namespace
│  │  └─1-Kubernetes集群Namespace
│  ├─7-kubernetes核心概念概述
│  │  ├─1-kubernetes核心概念
│  │  └─2-kubernetes核心概念之间的关系
│  ├─8-Kubernetes集群核心概念Pod
│  │  ├─1-Pod定义及分类
│  │  ├─2-Pod创建与删除
│  │  ├─3-Pod生命周期管理
│  │  └─4-Pod故障排除方法
│  └─9-Kubernetes集群核心概念Controller
│      ├─1-Controller作用及分类
│      ├─2-Deployment介绍及应用
│      ├─3-ReplicaSet介绍及应用
│      ├─4-DaemonSet介绍及应用
│      ├─5-StatefulSet介绍及应用
│      ├─6-Job介绍及应用案例
│      └─7-CronJob介绍及应用案例
├─08-Kubernetes服务暴露
│  ├─1-IngressNginxController
│  │  ├─1-ingress作用
│  │  ├─2-ingress控制器种类
│  │  ├─3-ingressnginxcontroller位置
│  │  ├─4-ingressnginxcontroller部署
│  │  ├─5-ingressnginxcontroller资源对象应用案例
│  │  ├─6-ingressnginxcontroller1.4.0
│  │  └─7-基于IngressNginx实现灰度发布
│  └─2-Ingress服务发现traefik
│      ├─1-traefik初识
│      ├─2-traefik部署
│      ├─3-traefikdashboard访问
│      ├─4-traefik基础应用
│      ├─5-traefik中间件
│      ├─6-traefik高级应用
│      └─7-KubernetesGatewayAPI
├─09-Kubernetes配置与密钥管理
│  ├─1-配置和密钥管理ConfigMap
│  │  └─1-Kubernetes配置与密钥管理ConfigMap
│  └─2-配置和密钥管理Secret
│      └─1-kubernetes配置与密钥管理Secret
├─10-Kubernetes容器镜像仓库管理方案
│  └─1-容器镜像仓库管理方案Harbor
│      └─1-kubernetes集群使用容器镜像仓库Harbor
├─11-Kubernetes安全机制
│  └─1-安全机制
│      ├─1-k8s安全管理安全框架
│      ├─2-k8s安全管理认证实践用户实践
│      ├─3-k8s安全管理认证实践集群认证
│      ├─4-k8s安全管理认证实践授权基础
│      └─5-k8s安全管理认证实践授权案例
├─12-Kubernetes存储解决方案
│  ├─1-kubernetes存储卷
│  │  ├─1-kubernetes存储卷
│  │  ├─2-PV与PVC
│  │  └─3-kubernetes存储动态供给
│  ├─2-存储解决方案GlusterFS
│  │  └─1-Kubernetes集群存储解决方案GlusterFS
│  └─3-存储解决方案Ceph
│      ├─1-Ceph分布式存储快速入门
│      ├─2-Ceph分布式存储核心实战
│      └─3-Ceph分布式存储综合实践
├─13-Kubernetes项目上云部署
│  ├─1-kubernetes集群公共服务
│  │  └─1-kubernetes集群公共服务
│  ├─2-项目部署JAVA项目
│  │  ├─1-项目部署前准备工作
│  │  ├─2-持久化存储准备工作
│  │  ├─3-项目容器镜像仓库及项目源码准备
│  │  ├─4-项目上云部署
│  │  └─5-项目部署访问验证
│  ├─3-项目部署Python项目
│  │  └─1-kubernetes集群python项目上云部署
│  └─4-项目部署GoLang项目
│      └─1-基于Golang开发百万并发IM即时消息系统
├─14-Kubernetes集群节点及Pod日志收集方案
│  ├─1-集群及Pod日志收集ELK
│  │  ├─1-收集日志必要性及收集方案介绍
│  │  ├─2-ELK集群部署及应用验证
│  │  └─3-使用ELK收集日志应用案例
│  └─2-集群及Pod日志收集EFK
│      ├─1-EFK介绍
│      └─2-EFK部署
├─15-Kubernetes云原生中间件上云部署
│  ├─1-企业级中间件类应用部署案例zookeeper
│  │  └─1-kubernetes云原生中间件上云部署zookeeper
│  ├─2-企业级中间件类应用部署案例kafka
│  │  └─1-kubernetes云原生中间件上云部署kafka
│  └─3-企业级中间件类应用部署案例rocketmq
│      ├─1-RocketMQ介绍
│      └─2-RocketMQ部署
├─16-Kubernetes云原生包管理方案
│  └─1-包管理方案Helm应用商店
│      ├─1-helm介绍
│      ├─2-helm基础使用
│      ├─3-helmchart包开发
│      └─4-helm应用商店Kubeapps
├─17-Kubernetes原生配置管理
│  └─1-Kubernetes原生配置管理Kustomize
│      └─1-Kubernetes原生配置管理Kustomize
├─18-kubernetes网络解决方案
│  ├─1-网络解决方案flannel
│  │  ├─1-kubernetes集群部署（flannel）
│  │  └─2-网络解决方案flannel方案
│  ├─2-网络解决方案calico
│  │  ├─1-k8s集群网络解决方案Calico方案之CNI方案
│  │  ├─2-k8s集群网络解决方案Calico部署
│  │  └─3-k8s集群网络解决方案Calico应用实战
│  ├─3-k8s集群underlay网络方案HybridNet
│  │  └─1-k8s集群underlay网络方案HybridNet
│  └─4-k8s集群双栈协议方案antrea(IPv4&IPv6)
│      └─1-k8s集群双栈协议方案antrea(IPv4&IPv6)
├─19-基于KubernetesPaaS云平台
│  ├─1-PaaS云平台rancher
│  │  ├─1-Rancher容器云管理平台
│  │  └─2-基于Kubernetes构建Rancher高可用平台
│  └─2-PaaS云平台kubesphere
│      ├─1-在Linux主机上以allinone模式安装Kubesphere
│      ├─2-在Kubernetes集群中安装Kubesphere
│      ├─3-KubeSphere多租户系统应用
│      └─4-KubeSphere应用发布初体验
├─20-主流公有云容器服务
│  ├─1-阿里云容器服务ACK
│  │  └─1-阿里云容器服务ACK初识
│  └─2-基于阿里云ECS自建K8S集群
│      └─1-基于阿里云ECS自建K8S集群
├─21-DevOps项目发布一体化平台构建及应用实践
│  ├─1-基于Kubernetes集群构建大中型企业CICD应用平台
│  │  ├─1-DevOps介绍
│  │  ├─10-Kubernetes编排工具
│  │  ├─2-Code阶段工具
│  │  ├─3-Build阶段工具
│  │  ├─4-Operate阶段工具
│  │  ├─5-Integrate工具
│  │  ├─6-Jenkins实现CI、CD操作
│  │  ├─7-SonarQube代码质量检测工具
│  │  ├─8-Harbor私有镜像仓库
│  │  └─9-Jenkins流水线
│  ├─2-基于KubeSphere构建企业新一代自动化CICD应用平台
│  │  ├─1-KubeSphereDevOps使用前账号准备
│  │  └─2-基于KubeSphere实现DevOps
│  └─3-云原生多云持续交付GitOps
│      ├─1-GitOps介绍
│      ├─2-GitOps系统实现
│      ├─3-GitOps项目案例
│      ├─4-ArgoCD部署（2.9.1）指南
│      ├─5-通过ArgoCD实现多K8S集群项目发布
│      └─6-通过Gitlab及ArgoCD实现项目发布
├─22-微服务项目部署
│  ├─1-sangomall微服务项目
│  │  ├─1-Kubernetes集群公共服务DNS
│  │  ├─2-Kubernetes集群公共服务Harbor
│  │  ├─3-负载均衡器OpenELB
│  │  ├─4-云原生微服务网关APISIX
│  │  ├─5-KubeSphere集成本地容器镜像仓库Harbor
│  │  ├─6-微服务中间件部署
│  │  ├─7-微服务项目部署准备
│  │  └─8-流水线部署微服务项目
│  └─2-严选微服务项目
│      ├─1-KubeSphere运行K8S集群部署
│      ├─10-严选商城项目中间件部署
│      ├─11-严选商城项目第三方服务申请
│      ├─12-严选商城项目配置导入及数据库导入
│      ├─13-严选项目流水线基础环境准备
│      ├─14-严选中台及商城项目流水线编写及项目发布
│      ├─15-严选前端项目流水线编写及项目发布
│      ├─2-K8S公共服务-DNS服务
│      ├─3-CoreDNS级联本地DNS服务
│      ├─4-K8S公共服务-容器镜像仓库服务Harbor
│      ├─5-KubeSphere部署
│      ├─6-KubeSphere多租户系统应用
│      ├─7-KubeSphere集成本地容器镜像仓库Harbor
│      ├─8-云原生负载均衡器OpenELB
│      └─9-云原生服务网关APISIX
├─23-云原生监控系统
│  ├─1-Prometheus监控
│  │  ├─1-二进制方式部署Prometheus监控系统
│  │  ├─2-二进制方式部署Prometheus监控系统告警
│  │  ├─3-容器化构建Prometheus监控系统
│  │  ├─4-容器监控方案CAdvisor
│  │  └─5-k8s监控方案KSM
│  ├─2-Prometheus监控
│  │  └─1-helm安装prometheus全家桶及应用案例
│  ├─3-K8S成本监控方案KubeCost
│  │  └─1-k8s成本监控方案
│  ├─4-应用性能管理APM平台Skywalking
│  │  └─1-应用性能监控APM平台Skywalking
│  ├─5-OpenTelemetry全链路状态跟踪
│  │  └─1-云原生应用全链路状态跟踪OpenTelemetry
│  └─6-云原生应用可观测方案Pixie
│      └─1-云原生应用可观测方案Pixie
├─24-微服务治理与服务网络
│  ├─1-服务治理之Istio(1.17版)
│  │  ├─1-Isito服务治理_大纲脉络
│  │  ├─2-Istio快速入门_istio基础
│  │  ├─3-Istio快速入门_Istio部署
│  │  ├─4-Istio快速入门_istio原理
│  │  └─5-Istio快速入门_流量基础
│  └─2-ServiceMesh实战之Istio
│      ├─1-istio概述
│      ├─10-istio熔断和故障注入
│      ├─11-istio流量镜像、可观测性
│      ├─2-istio基础环境安装
│      ├─3-istio安装和bookinfo安装
│      ├─4-istio组件介绍，kiali安装
│      ├─5-istio原理介绍
│      ├─6-istio流量管理和命名空间
│      ├─7-istio虚拟服务和目标规则
│      ├─8-istio超时，重试，以及灰度发布
│      └─9-istioessgateway
├─25-k8s多集群管理方案
│  ├─1-k8s多集群管理方案
│  │  ├─1-使用kubeconfig管理多集群
│  │  └─2-集群联邦karmada
│  ├─2-k8s集群舰队管理方案Kurator
│  │  └─1-K8S集群舰队管理
│  └─3-Cilium多集群方案ClusterMesh
│      └─1-Cilium多集群方案ClusterMesh
├─26-云原生应用备份与恢复方案
│  └─1-k8s集群备份与恢复利器Velero
│      └─1-使用Velero实现对云原生应用备、恢复、迁移
├─27-云计算下一个十年技术Serverless
│  ├─1-Serverless深度实战之Knative
│  │  ├─1-使用Knative平台环境说明
│  │  ├─10-Tekton全自动发布Knative平台应用案例
│  │  ├─11-Tekton应用_初体验
│  │  ├─12-Tekton应用_构建自定义Tag镜像应用案例
│  │  ├─13-Tekton应用_流水线中使用WorkSpace应用案例
│  │  ├─14-Tekton应用_使用DIND实现容器镜像构建应用案例
│  │  ├─15-Tekton应用_使用GitLabWebHook触发Tekton自动构建应用案例
│  │  ├─16-Tekton应用_使用Tekton实现自动流水线应用案例
│  │  ├─17-Tekton应用_Tekton与ArgoCD结合实现GitOps
│  │  ├─18-Knative平台应用可观测性
│  │  ├─19-Knative平台应用日志收集分析
│  │  ├─2-现阶段云原生应用领域介绍
│  │  ├─3-为什么要引入Serverless
│  │  ├─4-Serverless应用场景
│  │  ├─5-Serverless架构优缺点
│  │  ├─6-Knative介绍
│  │  ├─7-Knative在云原生应用领域的定位
│  │  ├─8-Knative与云原生平台的三个实践方式
│  │  └─9-Knative部署及应用案例
│  └─2-serverless之OpenFaaS函数即服务平台
│      ├─1-OpenFaaS介绍
│      ├─2-OpenFaaS运行基础环境
│      ├─3-使用Helm部署OpenFaaS及Gateway访问
│      ├─4-OpenFaaS使用初体验
│      ├─5-使用模板开发和部署Function
│      ├─6-开发并部署PythonFunction
│      └─7-OpenFaaS自动扩缩容
├─28-基于Kubernetes构建大数据生态圈
│  ├─1-基于Kubernetes部署Flink实时计算平台
│  │  ├─1-基于Kubernetes构建大数据生态圈之环境准备
│  │  └─2-基于Kubernetes部署实时计算平台Flink
│  ├─2-基于Kubernetes部署Spark实时计算平台
│  │  └─1-基于Kubernetes部署实时计算平台Spark
│  └─3-基于K8S构建机器学习平台KubeFlow
│      └─1-基于Kubernetes构建机器学习平台KubeFlow
├─29-云原生数据服务
│  └─1-基于K8S构建云原生数据基础设施平台KubeBlocks
│      └─1-云原生数据服务基础设施平台KubeBlocks
├─30-kubernetes应用二次开发
│  ├─1-基于win10打造K8S应用开发环境
│  │  └─1-基于win10打造k8s应用开发环境
│  ├─2-k8soperator应用开发实战理论篇
│  │  ├─1-让k8s的价值起飞
│  │  ├─2-认识k8soperator
│  │  └─3-揭开k8soperator的神秘面纱
│  ├─3-k8soperator应用开发实战理论篇
│  │  ├─1-让k8s的价值起飞
│  │  ├─2-认识k8soperator
│  │  └─3-揭开k8soperator的神秘面纱
│  ├─4-k8soperator应用开发实战进阶篇手撸SaaS站
│  │  └─1-手撸代码之世界知名SaaS站Heroku
│  ├─5-k8soperator应用开发实战进阶篇手撸SaaS站
│  │  └─1-手撸代码之世界知名SaaS站Heroku
│  ├─6-DevOps应用开发实战之CI-CD落地方案
│  │  └─1-ci-cd落地
│  └─7-云原生DevOps应用平台开发实战
│      └─1-CI-CDOperator开发
├─31-云原生边缘计算
│  └─1-云原生边缘计算KubeEdge
│      ├─1-k8s1.22版本集群部署
│      └─2-kubeedge部署
├─32-kubernetes管理虚拟机
│  └─1-kubernetes管理虚拟机利器KubeVirt
│      └─1-Kubernetes管理虚拟机利器KubeVirt
├─33-Golang开发入门精讲
│  └─1-Golang语法精讲
│      ├─1-马士兵老师介绍-go语言
│      ├─10-第5阶段：函数
│      ├─11-第5阶段：函数
│      ├─12-第6阶段：错误处理
│      ├─13-第7阶段：数组
│      ├─14-第8阶段：切片
│      ├─15-第9阶段：映射
│      ├─16-第10阶段：面向对象
│      ├─17-第10阶段：面向对象
│      ├─18-第11阶段：文件和操作
│      ├─19-第12阶段：协程和管道
│      ├─2-马士兵老师介绍-go语言中的面向对象
│      ├─20-第13阶段：网络编程
│      ├─21-第14阶段：反射
│      ├─3-第1阶段：走进Golang
│      ├─4-第1阶段：走进Golang
│      ├─5-第2阶段：变量与数据类型
│      ├─6-第2阶段：变量与数据类型
│      ├─7-第3阶段：运算符
│      ├─8-第4阶段：流程控制
│      └─9-第4阶段：流程控制
├─34-Kubernetes应用实战及源码剖析
│  └─1-kubernetes实战与源码剖析
│      ├─1-第1章准备工作
│      ├─10-第10章kubelet中的cgroupManager解读
│      ├─11-第11章kubelet中的资源管理器cpuManager、memoryManager、deviceManager解读
│      ├─12-第12章kubeletpleg对象和containerManager总结
│      ├─13-第13章kubeletcontainerRuntime和sandbox容器
│      ├─14-第14章containerRuntime创建init容器前期工作
│      ├─15-第15章创建init和app容器的后期工作
│      ├─16-第16章containerRuntime停止容器的流程
│      ├─17-第17章kubelet的GarbageCollection
│      ├─18-第18章kubelet的syncLoop的第1大监听configCh
│      ├─19-第19章kubelet的syncLoop的其余监听
│      ├─2-第2章创建pod时kubectl的执行流程和它的设计模式
│      ├─20-第20章kubelet中内置的cadvisor
│      ├─21-第21章kubelet中内置的dockershim机制
│      ├─22-第22章容器底层技术之镜像原理
│      ├─23-第23章k8sjob和cronjob源码解读
│      ├─24-第24章k8sdeployment源码解读
│      ├─25-第25章k8sReplicaSetController源码分析
│      ├─26-第26章k8sdaemonSet源码分析
│      ├─27-第27章k8sstatefulSet源码分析
│      ├─28-第28章Service的定义和概念
│      ├─29-第29章kube-proxyiptables和ipvs模式源码解读
│      ├─3-第3章apiserver中的权限相关
│      ├─30-第30章k8s网络底层原理
│      ├─31-第31章k8sIngress7层路由机制和traefik源码解读
│      ├─32-第32章k8s存储对象源码解读
│      ├─33-第33章k8sconfigMap和secret解析
│      ├─34-第34章k8shpa扩容和Aggregator汇聚插件原理解读
│      ├─35-第35章基于prometheus-adaptor的自定义指标HPA
│      ├─36-第36章k8svpa扩容
│      ├─37-第37章k8shpa和vpa依赖的metrics-server源码解读和kubelettop原理
│      ├─38-第38章k8scrd开发
│      ├─39-第39章istio上手使用和sidecar流量劫持原理解析
│      ├─4-第4章自定义准入控制器，完成nginxsidecar的注入
│      ├─40-第40章envoy基础知识
│      ├─41-第41章istio组件分析
│      ├─5-第5章API核心服务的处理流程
│      ├─6-第6章kube-scheduler调度pod的流程
│      ├─7-第7章kube-controller-manager控制管理中心的作用
│      ├─8-第8章kubelet节点上控制容器生命周期的管理者
│      └─9-第9章kubelet稳定性保证Eviction驱逐和oom
├─35-VIP直播课
│  └─1-云原生（K8S核心）架构师VIP直播
│      ├─1-云原生（K8S核心）架构师VIP直播
│      │  └─25-下一代容器镜像构建工具Buildkit
│      │      └─Part_0
│      └─2-2024-云原生VIP直播课
├─36-Prometheus应用实战及源码剖析
│  └─1-Prometheus-基础入门到源码剖析
│      ├─1-学习本课程的收益
│      ├─10-redis-exporter安装和使用
│      ├─11-java应用监控jvm实例
│      ├─12-pushgateway使用
│      ├─13-告警和alertmanager简单使用
│      ├─14-k8s监控难点分析
│      ├─15-k8s监控环境搭建，yaml讲解
│      ├─16-k8s容器基础资源指标采集原理和指标讲解
│      ├─17-k8s对象资源指标
│      ├─18-k8s服务组件指标
│      ├─19-k8s部署在pod中业务埋点指标
│      ├─2-学习目标
│      ├─20-分析pull模型在k8s中的应用，对比push模型
│      ├─21-k8s接口鉴权、认证和在监控中的实现
│      ├─22-k8s服务发现原理解析
│      ├─23-章k8s监控中标签relabel的应用和k8s监控总结
│      ├─24-主流服务发现类型介绍，监控系统和服务树CMDB如何打通
│      ├─25-如何降低采集资源消耗
│      ├─26-分位值作用和原理
│      ├─27-采集端高可用实战
│      ├─28-go实战项目动态分片解决pushgateway高可用
│      ├─29-如何使用非侵入式形式如日志接入prometheus
│      ├─3-安装prometheus和上手使用
│      ├─30-时序数据库存储模型
│      ├─31-facebook-gorilla压缩算法原理
│      ├─32-prometheus自研tsdb底层原理
│      ├─33-集群tsdb原理和实战（一）
│      ├─34-m3db原理和实战
│      ├─35-thanos项目和组件源码解读
│      ├─36-kube-prometheus和prometheus-operator原理和实战
│      ├─37-prometheus核心接口源码解析
│      ├─38-范围查询分阶段原理
│      ├─39-prometheus接口开发实战
│      ├─4-prometheus基本概念介绍
│      ├─40-高基数查询和prometheus预聚合原理和源码解读
│      ├─41-查询提速实战提升查询速度30-100倍
│      ├─42-告警触发prometheus源码解读和告警触发模块高可用方案
│      ├─43-alertmanager源码解读和实战
│      ├─44-告警回调实战
│      ├─5-node_exporter安装和使用
│      ├─6-grafana安装和使用
│      ├─7-黑盒探针blackbox_exporter安装和使用
│      ├─8-mysqld_exporter使用和源码改造
│      └─9-process-exporter安装和使用
├─37-容器云-云原生架构师面试宝典
│  └─2-kubernetes面试题
│      └─1-大厂kubernetes面试夺命九连问第一季
└─云原生架构师资料文件夹

```

