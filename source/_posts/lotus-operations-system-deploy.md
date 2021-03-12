---
title: lotus内部运维系统部署
top: true
cover: true
toc: true
mathjax: true
date: 2021-03-11 20:12:23
password:
summary:
tags:
- 部署文档
categories:
- 项目部署
---



# 版本说明

minercloud-v1.0.0

- minercloud：对应服务名称

- 第一位数字：对应需求，需求变更发版+1
- 第二位数字：对应功能，功能变更发版+1
- 第三位数字：对应bug，bug修复发版+1

# 1、公有云部署

## 1.1 安装mysql数据库

{% post_link mysql-install-ubuntu18.04 %}

## 1.2 安装redis数据库

{% post_link redis-install-ubuntu18.04 %}

## 1.3 安装公有云服务

```shell
// 1. 将公有云服务安装包导入到公有云服务器
// 2. 解压安装包
tar -xvmf publiccloud-v1.0.0.tar.gz
// 3. 执行安装脚本
// ./publiccloud/install.sh
```

## 1.4 修改配置文件

```shell
vim /usr/local/etc/publiccloud/config.yaml
```



# 2、集群云服务部署

每个集群部署一个minercloud到集群的云服务器

## 2.1 安装mysql数据库

{% post_link mysql-install-ubuntu18.04 %}

## 2.2 安装redis数据库

{% post_link redis-install-ubuntu18.04 %}

## 2.3 安装集群云服务

```shell
// 1. 将公有云服务安装包导入到公有云服务器
// 2. 解压安装包
tar -xvmf minercloud-v1.0.0.tar.gz
// 3. 执行安装脚本
// ./minercloud/install.sh
```

## 2.4 修改配置文件

```shell
vim /usr/local/etc/minercloud/config.yaml
// 修改以下配置内容
```



# 3、升级矿机基础软件服务

## 3.1 批量升级矿机基础服务

- 把update_device.tar.gz传到集群一台机器，tar -xvmf update_device.tar.gz解压 

- 使用批量升级脚本update_device.sh,在脚本中输入机器列表，执行脚本

  

- 选择对应矿工执行升级即可