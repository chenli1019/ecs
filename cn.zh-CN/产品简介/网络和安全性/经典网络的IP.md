# 经典网络的IP {#concept_lky_f3w_ydb .concept}

IP地址是您访问ECS实例或者您的用户访问部署在ECS实例的服务的主要方式。目前经典网络IP地址由阿里云统一分配，分为公网IP地址和内网IP地址。

## 内网IP地址 {#section_dlg_g3w_ydb .section}

每台经典网络类型的ECS实例一定会被分配一个IP地址用于内网通信，这个IP地址被称为内网IP地址。

**应用场景**

内网IP地址可以用于以下情况：

-   负载均衡
-   同一局域网内ECS实例之间内网互访
-   同一局域网内ECS实例与其他云服务（如OSS、RDS）之间内网互访

内网通信产生的流量免费。关于更多内网通信的信息，参见 [内网](cn.zh-CN/产品简介/网络和安全性/内网.md#)。

**修改内网IP地址**

经典网络类型ECS实例一经创建，不能在ECS管理控制台上修改内网IP地址。

**说明：** 不能在操作系统内部自行变更内网IP地址，否则会导致内网通讯中断。

## 公网IP地址 {#section_hlg_g3w_ydb .section}

如果您购买了公网带宽（即公网带宽不为0 Mbit/s），阿里云会为您的实例分配一个公网IP地址。经典网络的公网IP地址一旦分配，不可更改。

**应用场景**

公网IP地址可以用于以下情况：

-   ECS实例与Internet之间互访
-   不在同一局域网内的ECS实例与其他阿里云产品之间互访

**获取方式**

在 创建ECS实例 时，无论采用哪种计费方式，只要您选择 **分配公网IP地址**，您的实例就会分配一个公网IP地址。

预付费实例，如果在创建时未分配公网IP地址，您可以通过 升级配置 或 续费降配 将公网带宽值设为一个非零值来分配公网IP地址。

**说明：** 

-   按量付费的经典网络类型ECS实例：如果在创建实例时未分配公网IP地址，不能再分配公网IP地址。
-   经典网络类型ECS实例：公网IP地址一经分配，既不能释放，也不能解绑。即使您通过 续费降配 或者 按量实例更改带宽 等功能将公网带宽值设为0 Mbit/s，公网IP地址仍会保留，只是您的实例不能访问公网。

**计费**

阿里云只对公网出网带宽收取费用，入网带宽免费。更多公网带宽的计费信息，参见 产品定价-公网带宽计费。

## 组播和广播 {#section_nlg_g3w_ydb .section}

内网IP地址不支持组播和广播。

