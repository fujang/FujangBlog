# FujangBlog

## 一、项目信息

A beautiful &amp; simple blog system based on SSM.

+ 该博客是基于SSM实现的个人博客系统，适合初学SSM和个人博客制作的同学学习。最新版本支持用户注册，包含用户和管理员两个角色 。

+ 主要涉及技术包括的包括Maven、Spring、SpringMVC、MyBatis、JSP、MySQL等。

## 二、预览图

### 1. 博客前端

### 2. 登录界面

### 3. 博客后台

## 三、项目部署

1. 克隆项目：分为三部分：``FujangBlog``文件(项目主体)、``uploads``文件(项目图片等资源)、``forest_blog.sql``文件(创建数据库且加载数据)。

2. 导入IDEA的Maven项目

3. 创建数据库``forest_blog``且导入sql文件。

4. 修改项目中的数据库连接信息(``db.properties``)

5. 配置tomcat和uploads目录：在tomcat的Deployment中增加``uploads``文件，可以将``uploads``文件放入D盘中，或手动更改项目中此文件的引用位置。

6. 将``Application context``更改为``/``。

   
