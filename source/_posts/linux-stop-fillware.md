---
title: Linux关闭防火墙命令
top: true
cover: false
toc: true
mathjax: true
date: 2021-03-11 17:18:23
password:
summary:
tags:
- linux
categories:
- 命令
---

# Linux关闭防火墙命令

问题:老是关闭防火墙太麻烦，所以选择彻底关闭防火墙，发现每次都记不住命令!

## 查看防火状态

```shell
systemctl status firewalld

service  iptables status
```

## 暂时关闭防火墙

```shell
systemctl stop firewalld

service  iptables stop
```

## 永久关闭防火墙

```shell
systemctl disable firewalld

chkconfig iptables off
```

## 重启防火墙

```shell
systemctl enable firewalld

service iptables restart 
```

