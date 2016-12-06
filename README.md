# JAVA-SSM-Spring
Spring + Maven + MyBatis + JUnit完美组合

_
tips: 启动项目后，welcome-file的链接即为测试用例

详细描述:http://blog.csdn.net/djy1992/article/details/52335321

部署maven web项目
Eclipse使用Maven构建web项目详解
pom.xml添加webapp依赖：
<dependency>
    <groupId>javax.servlet</groupId>
    <artifactId>javax.servlet-api</artifactId>
    <version>3.1.0</version>
    <scope>provided</scope>
</dependency>
<dependency>
    <groupId>javax.servlet</groupId>
    <artifactId>jsp-api</artifactId>
    <version>2.0</version>
    <scope>provided</scope>
</dependency>
<dependency>
    <groupId>javax.servlet</groupId>
    <artifactId>jstl</artifactId>
    <version>1.2</version>
    <scope>provided</scope>
</dependency>
配置jdk版本，在build->plugins节点中添加：
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-compiler-plugin</artifactId>
    <configuration>
        <source>1.7</source>
        <target>1.7</target>
    </configuration>
</plugin>
整合spring
整合log4j
配置dataSource
Spring整合阿里巴巴开源数据源Druid
<!-- druid -->
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>druid</artifactId>
    <version>1.0.7</version>
</dependency>
编程方式取得Spring上下文的Properties
driverClassName=com.mysql.jdbc.Driver
url=jdbc:mysql://localhost:3306/ssm?useUnicode=true&characterEncoding=utf-8
整合mybatis
mybatis-spring官方文档 - SqlSessionFactoryBean > 在此，应完成的有： > 1. 事务管理 > 2. 扫描mapper包
整合mybatis-generator
MyBatis Generator generatorConfig.xml配置详解 > mybatis-spring的版本换成1.3.0，否则会报错： > java.lang.AbstractMethodError: org.mybatis.spring.transaction.SpringManagedTransaction.getTimeout()L
用Maven插件生成Mybatis代码
用junit测试一下
Junit测试用例见test下的cn.jxnu.mapper.UserMapperTest
Spring Test+JUnit完美组合
整合springMVC
spring MVC配置详解
