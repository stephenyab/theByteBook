# 第四章：负载均衡概论与实践

负载均衡是构建可靠的分布式系统最核心的概念之一。几乎所有的大型分布式系统都是用四层负载均衡（例如 LVS、DPVS）基于 OSPF 协议实现多活入口，入口后方为七层负载均衡（例如 OpenResty、Kong、APISIX 等）实现的网关服务。这些服务与基础架构层组件，例如弹性伸缩、自动化扩容服务等协同工作，实现业务系统高可用、高性能、高并发目标。

不过无论负载均衡以何种形式存在，核心的职责都是“选择谁来处理用户请求”和“将用户请求转发过去”，本章我们就从这两个角度讲解负载均衡。