# README
参考([mall](http://www.macrozheng.com/#/))学习，还需要进一步学习各类各种技术。
- spring boot 2.5.7
- MongoDB 
- Redis
- elasticsearch
- RabbitMQ




> `pom.xml`的配置

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>2.5.7</version>
		<relativePath/> <!-- lookup parent from repository -->
	</parent>
	<groupId>com.lw.mall</groupId>
	<artifactId>demo</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<name>demo</name>
	<description>Demo project for Spring Boot</description>
	<properties>
		<java.version>11</java.version>
	</properties>
	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>		
		<dependency>
			<groupId>org.projectlombok</groupId>
			<artifactId>lombok</artifactId>
			<scope>annotationProcessor</scope>
		</dependency>
		<!-- import annotation of @NotEmpty() -->
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-validation</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>

        <!--MyBatis分页插件-->
        <dependency>
            <groupId>com.github.pagehelper</groupId>
            <artifactId>pagehelper-spring-boot-starter</artifactId>
            <version>1.2.10</version>
        </dependency>
        <!--集成druid连接池-->
        <dependency>
            <groupId>com.alibaba</groupId>
            <artifactId>druid-spring-boot-starter</artifactId>
            <version>1.1.10</version>
        </dependency>
        <!-- MyBatis 生成器 -->
        <dependency>
            <groupId>org.mybatis.generator</groupId>
            <artifactId>mybatis-generator-core</artifactId>
            <version>1.3.3</version>
        </dependency>
        <!--Mysql数据库驱动-->
        <dependency>
            <groupId>mysql</groupId>
            <artifactId>mysql-connector-java</artifactId>
			<scope>runtime</scope>
        </dependency>
		<!-- Swagger-UI API文档生产工具 3.0版本
		<dependency>
		<groupId>io.springfox</groupId>
		<artifactId>springfox-boot-starter</artifactId>
		<version>3.0.0</version>
		</dependency> -->
        <!--Swagger-UI API文档生产工具-->
        <dependency>
            <groupId>io.springfox</groupId>
            <artifactId>springfox-swagger2</artifactId>
            <version>2.9.2</version>
        </dependency>
        <dependency>
            <groupId>io.springfox</groupId>
            <artifactId>springfox-swagger-ui</artifactId>
            <version>2.9.2</version>
        </dependency>
        <!--解决Swagger 2.9.2版本NumberFormatException-->
        <dependency>
            <groupId>io.swagger</groupId>
            <artifactId>swagger-models</artifactId>
            <version>1.6.0</version>
        </dependency>
        <dependency>
            <groupId>io.swagger</groupId>
            <artifactId>swagger-annotations</artifactId>
            <version>1.6.0</version>
        </dependency>
		<!-- redis -->
		<dependency>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-data-redis</artifactId>
		</dependency>
        <!--统一Guava版本防止冲突-->
        <dependency>
            <groupId>com.google.guava</groupId>
            <artifactId>guava</artifactId>
            <version>31.0.1-jre</version>
        </dependency>
		<!--SpringSecurity依赖配置-->
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-security</artifactId>
		</dependency>
		<!--Hutool Java工具包-->
		<dependency>
			<groupId>cn.hutool</groupId>
			<artifactId>hutool-all</artifactId>
			<version>4.5.7</version>
		</dependency>
		<!--JWT(Json Web Token)登录支持-->
		<dependency>
			<groupId>io.jsonwebtoken</groupId>
			<artifactId>jjwt</artifactId>
			<version>0.9.1</version>
		</dependency>
		<!-- 添加依赖 解决 ClassNotFoundException: javax.xml.bind.DatatypeConverter-->
		<dependency>
			<groupId>javax.xml.bind</groupId>
			<artifactId>jaxb-api</artifactId>
			<version>2.3.1</version>
		</dependency>
		<!--Elasticsearch相关依赖-->
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-elasticsearch</artifactId>
		</dependency>
		<!---mongodb相关依赖-->
		<dependency>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-data-mongodb</artifactId>
		</dependency>
		<!--消息队列相关依赖-->
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-amqp</artifactId>
		</dependency>
		<dependency>
			<groupId>org.aspectj</groupId>
			<artifactId>aspectjweaver</artifactId>
		</dependency>
	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
		</plugins>
	</build>
</project>
```

> 关于spring2.6之后不允许循环依赖的问题，`application.yml`添加配置项

``` yaml
spring:
  main:
    allow-circular-references: true
```


> Mybatis Generator用到的配置文件`generator.properties`
``` properties
jdbc.driverClass=com.mysql.cj.jdbc.Driver
jdbc.connectionURL=jdbc:mysql://<ip>:<port>/<database nema>?useUnicode=true&characterEncoding=utf-8&serverTimezone=Asia/Shanghai&useSSL=false
jdbc.userId=root
jdbc.password=root
```



安装的一些工具目录:

> `MongDB`: 
>
> `path`: `C:\Program Files\MongoDB\`

> `elasticsearch`:
>
> `path`:`D:\software\elasticsearch-7.16.2-windows-x86_64`

> `kibana`:
>
> `path`: `D:\software\elasticsearch-7.16.2-windows-x86_64\kibana-7.16.2-windows-x86_64`

> `ik`:  中文分词器，`elasticsearch`不支持中文分词.
>
> `path`：`D:\software\elasticsearch-7.16.2-windows-x86_64\elasticsearch-7.16.2\plugins`

> `redis`: asd 
>
> `path`: `D:\software\Redis-x64-5.0.14`
> `运行方法`: `.\redis-server.exe redis.windows.conf`

> `erlang`: `D:\software\erlang\erl-24.2`

> `rabbitmq`: `D:\software\rabbitmq\rabbitmq_server-3.9.11`
>
> ``` shell
> rabbitmq-service.bat remove
> set RABBITMQ_BASE=D:\Program Files\RabbitMQ\soft\rabbitmq_server-3.7.18\data
> rabbitmq-service.bat install
> rabbitmq-plugins enable rabbitmq_management
> 
> rabbitmq-server restart
> ```
> 访问 [管理页面](localhost:15672) 

