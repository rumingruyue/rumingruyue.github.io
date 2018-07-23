---
title: 远程debug技巧
date: 2018-07-23 12:58:51
tags:
- 编程
- 技巧 
categories:
- 编程 
---
IDEA远程debug配置

1、去tomcat 虚拟机参数下查看端口
`agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=37086`

2、填入端口和IP
{% asset_img debug.png debug配图 %}
3、打断点
如果断点上有对号，则说明打断点成功

ps:调试时如果断点不生效主要有以下几种情况：
1、 代码版本不一致
2、 选错了远程调试的项目（tomcat）


