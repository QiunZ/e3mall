# 宜立方商城项目学习
## 一、项目准备

### 1、系统架构

- 功能介绍
- 架构讲解：从传统架构到基于soa的架构

### 2、后台工程搭建

1. 工程分类
   - e3-parent：所有工程的父工程，定义版本号
   - e3-common：工具工程，定义通用工具和pojo等
   - e3-manager：聚合工程，下有
     - e3-manager-pojo
     - e3-manager-dao
     - e3-manager-interface
     - e3-manager-service
     - e3-manager-web
2. 使用maven搭建工程
3. 使用maven的tomcat插件启动工程

### 3、SSM框架整合

## 二、项目改造

### 1、服务中间件dubbo

1. dubbo和zookeeper的安装和使用
   - 在linux系统中安装zookeeper
   - 在项目pom.xml文件中引入dubbo依赖，需要注意dubbo所依赖spring版本过低的问题，在配置文件中将其排除

### 2、项目改造为基于SOA架构

- 主要是将e3-manager-web从e3-manager中抽取出来，作为表现层，e3-manager作为服务层，中间使用dubbo通信

### 3、测试

- 商品列表查询功能实现