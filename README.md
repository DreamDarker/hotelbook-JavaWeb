## 一、概述

酒店管理系统，类 Maven 项目结构。项目配置项为：

* 服务器：apache-tomcat-9.0.0.M26

* 数据库：Mysql

* 编辑器：IntelliJ IDEA

## 二、介绍

项目具体说明：[【Wiki】](https://github.com/inkss/hotelbook-JavaWeb/wiki)

JavaWeb 作业，即简单的酒店管理系统。

后端 Java 部分采用 MVC 形式，前端网页主要借鉴 [layui](http://www.layui.com) 与 [win10-ui](http://win10ui.yuri2.cn) 。

目前完成：登录，楼层，房间类型，预订单，日志的增删改查。网页前端功能反倒是全部划分完成。

整体写的七七八八，用了不少第三方的 jar 包，虽然采用了类似Maven的结构，但是本身只是普通的 JavaWeb 项目。

数据库脚本位于`~/src/sql`目录中，导入 mysql 后，用 IDEA 打开重新配置一下 JDK 与 Tomcat 不出意外是可以直接使用的。

附1：Tomcat 的  Deployment 中 Application context值为 /hb 

附2：数据库默认登录账号 root toor

重要：本项目最初是在 Ubuntu 上写的，中间才迁移到 Windows 上，所以数据库上踩了一个坑，Windows 对大小写不敏感，也就是 **Windows 不区分大小写**，数据库建表时表名称含有大写值，对应的就是 DAO 层操控数据库时表名也全是大写，但是在 Windows 下导出的表结构中表名**全是小写**，这里务必注意务必注意务必注意。从某种意义上来说这是数据库设计上遗留的问题。


