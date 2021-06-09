<!-- vscode-markdown-toc -->
* 1. [一、项目信息](#)
* 2. [二、预览图](#-1)
	* 2.1. [1. 博客前端](#-1)
	* 2.2. [2. 登录界面](#-1)
	* 2.3. [3. 博客后台](#-1)
* 3. [三、项目部署](#-1)
* 4. [四、项目配置文件介绍](#-1)
	* 4.1. [1、pom文件](#pom)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->
# FujangBlog

##  1. <a name=''></a>一、项目信息

A beautiful &amp; simple blog system based on SSM.

+ 该博客是基于SSM实现的个人博客系统，适合初学SSM和个人博客制作的同学学习。最新版本支持用户注册，包含用户和管理员两个角色 。

+ 主要涉及技术包括的包括Maven、Spring、SpringMVC、MyBatis、JSP、MySQL等。

##  2. <a name='-1'></a>二、预览图

###  2.1. <a name='-1'></a>1. 博客前端
![](https://github.com/fujang/FujangBlog/blob/master/else/photos/P1.png)
###  2.2. <a name='-1'></a>2. 登录界面
![](https://github.com/fujang/FujangBlog/blob/master/else/photos/P2.png)
###  2.3. <a name='-1'></a>3. 博客后台
![](https://github.com/fujang/FujangBlog/blob/master/else/photos/P3.png)

##  3. <a name='-1'></a>三、项目部署

1. 克隆项目：分为三部分：``FujangBlog``文件(项目主体)、``uploads``文件(项目图片等资源)、``forest_blog.sql``文件(创建数据库且加载数据)。

2. 导入IDEA的Maven项目

3. 创建数据库``forest_blog``且导入sql文件。

4. 修改项目中的数据库连接信息(``db.properties``)

5. 配置tomcat和uploads目录：在tomcat的Deployment中增加``uploads``文件，可以将``uploads``文件放入D盘中，或手动更改项目中此文件的引用位置。

6. 将``Application context``更改为``/``。

##  4. <a name='-1'></a>四、项目配置文件介绍

+ pom文件

+ web.xml文件

+ spring配置文件：spring-mvc.xml、spring-mybatis.xml

+ mybatis配置文件：mybatis-config.xml

+ mapper文件

+ db.properties文件

+ logback.xml文件

###  4.1. <a name='pom'></a>1、pom文件

lombok依赖，此依赖会帮助我们自动在字节码文件中生成带有``Data``注解的类的``Get/Set``等方法。

```xml
        <dependency>
                    <groupId>org.projectlombok</groupId>
                    <artifactId>lombok</artifactId>
                    <version>1.16.22</version>
        </dependency>
```

Servlet和Jsp依赖。

```xml
        <dependency>
            <groupId>javax.servlet</groupId>
            <artifactId>javax.servlet-api</artifactId>
            <version>3.1.0</version>
            <scope>provided</scope>
        </dependency>

        <!-- 添加jsp支持 -->
        <dependency>
            <groupId>javax.servlet.jsp</groupId>
            <artifactId>javax.servlet.jsp-api</artifactId>
            <version>2.3.1</version>
        </dependency>
```

JSTL标签库依赖。

```cml
        <dependency>
            <groupId>javax.servlet</groupId>
            <artifactId>jstl</artifactId>
            <version>1.1.2</version>
        </dependency>
        <dependency>
            <groupId>taglibs</groupId>
            <artifactId>standard</artifactId>
            <version>1.1.2</version>
        </dependency>
```

Spring依赖。

```xml
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-core</artifactId>
            <version>${spring.version}</version>
        </dependency>
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-beans</artifactId>
            <version>${spring.version}</version>
        </dependency>
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-context</artifactId>
            <version>${spring.version}</version>
        </dependency>
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-context-support</artifactId>
            <version>${spring.version}</version>
        </dependency>
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-web</artifactId>
            <version>${spring.version}</version>
        </dependency>
        <!--spring test支持-->
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-test</artifactId>
            <version>${spring.version}</version>
        </dependency>
        <!--spring mvc支持-->
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-webmvc</artifactId>
            <version>${spring.version}</version>
        </dependency>

        <!--spring 事务管理支持-->
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-tx</artifactId>
            <version>${spring.version}</version>
        </dependency>
        <!--spring jdbc操作支持-->
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-jdbc</artifactId>
            <version>${spring.version}</version>
        </dependency>
        <!--spring aop编程支持-->
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-aop</artifactId>
            <version>${spring.version}</version>
        </dependency>
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-aspects</artifactId>
            <version>${spring.version}</version>
        </dependency>
```

Mybatis依赖。

```xml
        <dependency>
            <groupId>org.mybatis</groupId>
            <artifactId>mybatis</artifactId>
            <version>3.4.0</version>
        </dependency>
        <dependency>
            <groupId>org.mybatis</groupId>
            <artifactId>mybatis-spring</artifactId>
            <version>1.3.0</version>
        </dependency>
```

JDBC驱动依赖。

```xml
        <dependency>
            <groupId>mysql</groupId>
            <artifactId>mysql-connector-java</artifactId>
            <version>8.0.11</version>
        </dependency>	
```

Druid连接池依赖。

```xml
        <dependency>
            <groupId>com.alibaba</groupId>
            <artifactId>druid</artifactId>
            <version>1.0.16</version>
        </dependency>
```

logback日志依赖。

```xml
        <dependency>
            <groupId>ch.qos.logback</groupId>
            <artifactId>logback-classic</artifactId>
            <version>1.1.2</version>
        </dependency>
        <dependency>
            <groupId>ch.qos.logback</groupId>
            <artifactId>logback-core</artifactId>
            <version>1.1.2</version>
        </dependency>
        <dependency>
            <groupId>org.logback-extensions</groupId>
            <artifactId>logback-ext-spring</artifactId>
            <version>0.1.1</version>
        </dependency>
```

Junit依赖。

```xml
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>4.12</version>
            <scope>test</scope>
        </dependency>	
```

文件上传组件依赖。

```xml
        <dependency>
            <groupId>commons-fileupload</groupId>
            <artifactId>commons-fileupload</artifactId>
            <version>1.3.3</version>
        </dependency>
```

Commons-io工具类依赖。

```xml
        <dependency>
            <groupId>commons-io</groupId>
            <artifactId>commons-io</artifactId>
            <version>2.4</version>
        </dependency>
```

jackson依赖。

```xml
        <dependency>
            <groupId>com.fasterxml.jackson.core</groupId>
            <artifactId>jackson-databind</artifactId>
            <version>${jackson-databind-version}</version>
        </dependency>
        <dependency>
            <groupId>com.fasterxml.jackson.core</groupId>
            <artifactId>jackson-core</artifactId>
            <version>${jackson-databind-version}</version>
        </dependency>
        <dependency>
            <groupId>com.fasterxml.jackson.core</groupId>
            <artifactId>jackson-annotations</artifactId>
            <version>${jackson-databind-version}</version>
        </dependency>
```

json依赖。

```xml
        <dependency>
            <groupId>org.json</groupId>
            <artifactId>json</artifactId>
            <version>20170516</version>
        </dependency>
```

Mybatis分页依赖。

```xml
        <dependency>
            <groupId>com.github.pagehelper</groupId>
            <artifactId>pagehelper</artifactId>
            <version>4.2.1</version>
        </dependency>
```

hutool工具包依赖。

```xml
        <dependency>
            <groupId>cn.hutool</groupId>
            <artifactId>hutool-all</artifactId>
            <version>4.1.13</version>
        </dependency>
```

fastjson依赖。

```xml
        <dependency>
            <groupId>com.alibaba</groupId>
            <artifactId>fastjson</artifactId>
            <version>1.2.72</version>
        </dependency>
```

guave依赖(避免造轮子)。

```xml
        <dependency>
            <groupId>com.google.guava</groupId>
            <artifactId>guava</artifactId>
            <version>26.0-jre</version>
        </dependency>
```

代码生工具依赖。

```xml
        <dependency>
            <groupId>com.googlecode.rapid-framework</groupId>
            <artifactId>rapid-core</artifactId>
            <version>4.0.5</version>
        </dependency>
```






















































