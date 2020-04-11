# Steam Cloud

[English](README.md)

[中文文档](README-zh_cn.md)

## 关联项目

后端: [steam-cloud](https://github.com/rosky/steam-cloud)

前端: [steam-cloud-ui](https://github.com/rosky/steam-cloud-ui)

## 概述

    🚀 不只是一个微服务快速开发框架。

## 可用状态

    目前开发中，非生产可用。

# 总则

项目以 *成长*，*快速*，*可控* 为原则。兼顾团队与个人、项目和企业。

对于具体技术选型，保持开放性，我们将选用经过市场考验的主流技术与最佳实践。但不纠结细节，每一个业务都有相应的特点，比如大并发下的技术架构，需针对性解决。

* 合适的技术 > 主流的技术 > 最新的技术
* 面向团队 > 面向招聘 > 面向未来
* 横向扩展支持 > 性能极限优化
* 业务流程优化 > 技术架构调整

## 团队

* 架构与创新团队：
  * 提供基础架构
  * 创新性技术研究
* 产品与设计团队：
  * 需求调研
  * 产品规划
  * 用户体验
* 程序与开发团队
  * 前端开发
  * 后端开发
  * 中台系统
* 测试与质量团队
  * 功能与自动化测试
  * 性能与自动化测试
  * 验收与自动化测试
* 运维与服务团队
  * 基础平台保障
  * 技术支持

## 代码规范

* Alibaba Java Coding Guidelines
* Airbnb JavaScript Style Guide

## 功能预览:

![steam-cloud](./images/steam-cloud.png)

# 入门

## 准备工作

### 开发环境

* Linux

* JAVA 8

* IntelliJ IDEA IDE

### Sentinel

* 在[这里](http://edas-public.oss-cn-hangzhou.aliyuncs.com/install_package/demo/sentinel-dashboard.jar)下载 DEMO 版文件

* 在[这里](https://github.com/alibaba/Sentinel/releases)下载 正式 版文件

运行：

```
java -jar sentinel-dashboard.jar
```

管理控制台：

正式版默认登陆:

* 用户名: sentinel

* 密码: sentinel

```
http://127.0.0.1:8080/
```

### Nacos

* 在[这里](https://github.com/alibaba/nacos/releases)下载 正式 版文件

运行：

```
unzip nacos-server-1.0.0.zip
cd nacos/bin
sh startup.sh -m standalone
```

管理控制台：

```
http://127.0.0.1:8848/nacos
```

### RocketMQ

* 在[这里](https://github.com/apache/rocketmq/releases)下载 正式 版文件

运行：

```
unzip rocketmq-all-4.7.0.zip
cd rocketmq-all-4.7.0

# Startup Name Server
sh bin/mqnamesrv

# Startup Broker
sh bin/mqbroker -n localhost:9876

# Create topic: test-topic
sh bin/mqadmin updateTopic -n localhost:9876 -c DefaultCluster -t test-topic
```

## Start projects

已测试运行正常:
```
SentinelServiceApplication :28083/
NacosDiscoveryConsumerSCLBApplication :18083/
DemoApplication :58070/
DubboSpringCloudServletGatewayBootstrap :61178/
DubboSpringCloudWebProviderBootstrap :9090/
NacosGatewayDiscoveryApplication :18085/
RocketMQBusApplication :38080/
SentinelDubboConsumerApp
SentinelDubboProviderApp
SentinelSpringCloudGatewayApplication :28085/
SentinelWebFluxApplication :28084/
SentinelZuulApplication :28086/
SpringCloudConfigClientApplication :28080/
SpringCloudConfigServerApplication :7070/
RocketMQConsumerApplication
SentinelFeignConsumerApplication :18087/
SentinelFeignProviderApplication :18088/
RocketMQProducerApplication :38081/
NacosConfigApplication :18084/
```

未测试:

```
DubboSpringCloudClientBootstrap
DubboSpringCloudConsumerBootstrap
DubboSpringCloudProviderBootstrap
DubboSpringCloudServerBootstrap
```

## Reference

趋势（影响我们选择 SCA 的重要因素）:

![trend-of-sca](./images/trend-of-sca.png)

主要特性:

![features-of-sca](./images/features-of-sca.png)

架构图:

![architecture-of-sca](./images/architecture-of-sca.png)

Sentinel 特性:

![features-of-sentinel](./images/features-of-sentinel.png)

Sentinel 开源生态:

![ecosystem-landscape-of-sentinel](./images/ecosystem-landscape-of-sentinel.png)

## 贡献人员

还缺你。
