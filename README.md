# GuliSchool(谷粒学院)



## 项目描述

谷粒学院项目是在线教育项目，采用B2C商业模块，使用微服务架构，采用前后端分离开发



## 项目功能模块

该项目分为前台系统和后台系统。



### 前台系统功能模块：



#### 首页数据显示

1. 显示幻灯片功能
2. 显示热门课程
3. 显示名师



#### 课程列表和详情

1. 条件查询分页列表功能
2. 课程信息显示（包含课程基本信息，分类，讲师，课程大纲）



#### 讲师列表和详情

1. 条件查询分页列表功能
2. 讲师基本信息和所讲课程



#### 登录注册

登录实现流程：登录调用登录接口返回token字符串，把返回token字符串放到cookie里面，创建前端拦截器进行判断，如果cookie里面包含token字符串，把token字符串放到header里面。调用接口根据token获取用户信息，把用户信息放到cookie里面，进行显示



### 后台系统功能模块：



#### 讲师管理模块

条件查询分页列表、添加、修改、删除



#### 课程管理模块

1. 课程列表功能
2. 添加课程



#### 课程分类模块

1. 添加课程分类：读取Excel里面课程分类数据，添加到数据库
2. 课程分类列表：使用树形结构显示课程分类列表



## 技术点

SpringBoot

SpringCloud (Nacos, Feign, Hystrix)

MyBatisPlus

EasyExcel

Redis

JWT

nginx



## 运行项目

1. 启动mysql5.7, 创建数据库guli, 执行数据库脚本
2. 启动nacos, redis, nginx
3. idea打开guli_parent, 启动eduApplication, ServiceAclApplication, UcenterApplication, CmsApplication模块
4. 打开vue-admin, vue-front, 运行`npm install` `npm run dev`



## todo

- Gateway网关替换nginx
- 后台登录模块和系统权限管理模块 (springsecurity框架)
