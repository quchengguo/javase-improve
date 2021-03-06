## 使用实现类方式整合spring-mybatis
1. 添加mybatis和spring jar包相关依赖
```
<dependencies>
    <!--junit4.12版本有错-->
  	<dependency>
	    <groupId>junit</groupId>
	    <artifactId>junit</artifactId>
	    <version>4.9</version>
	    <scope>test</scope>
	</dependency>
  	<!-- 日志相关jar包 -->
	<dependency>
	    <groupId>org.bgee.log4jdbc-log4j2</groupId>
	    <artifactId>log4jdbc-log4j2-jdbc4.1</artifactId>
	    <version>1.16</version>
	</dependency>
	<dependency>
	    <groupId>org.slf4j</groupId>
	    <artifactId>slf4j-api</artifactId>
	    <version>1.7.13</version>
	</dependency>
	<dependency>
	    <groupId>org.slf4j</groupId>
	    <artifactId>slf4j-log4j12</artifactId>
	    <version>1.7.5</version>
	</dependency>
	<dependency>
	    <groupId>log4j</groupId>
	    <artifactId>log4j</artifactId>
	    <version>1.2.16</version>
	</dependency>
	<!-- spring一套 -->
	<dependency>
		<groupId>org.springframework</groupId>
		<artifactId>spring-context</artifactId>
		<version>4.2.4.RELEASE</version>
	</dependency>
  	<dependency>
		<groupId>org.springframework</groupId>
		<artifactId>spring-core</artifactId>
		<version>4.2.4.RELEASE</version>
	</dependency>
	<dependency>
		<groupId>org.springframework</groupId>
		<artifactId>spring-beans</artifactId>
		<version>4.2.4.RELEASE</version>
	</dependency>
	<dependency>
		<groupId>org.springframework</groupId>
		<artifactId>spring-expression</artifactId>
		<version>4.2.4.RELEASE</version>
	</dependency>
	<dependency>
	    <groupId>org.springframework</groupId>
	    <artifactId>spring-web</artifactId>
	    <version>4.2.4.RELEASE</version>
	</dependency>
	<dependency>
	    <groupId>aopalliance</groupId>
	    <artifactId>aopalliance</artifactId>
	    <version>1.0</version>
	</dependency>
	<dependency>
	    <groupId>org.aspectj</groupId>
	    <artifactId>aspectjweaver</artifactId>
	    <version>1.6.8</version>
	</dependency>
	<dependency>
	    <groupId>org.springframework</groupId>
	    <artifactId>spring-aop</artifactId>
	    <version>4.2.4.RELEASE</version>
	</dependency>
	<dependency>
	    <groupId>org.springframework</groupId>
	    <artifactId>spring-aspects</artifactId>
	    <version>4.2.4.RELEASE</version>
	</dependency>
	<dependency>
	    <groupId>org.springframework</groupId>
	    <artifactId>spring-test</artifactId>
	    <version>4.2.4.RELEASE</version>
	    <scope>test</scope>
	</dependency>
  	<dependency>
	    <groupId>org.springframework</groupId>
	    <artifactId>spring-jdbc</artifactId>
	    <version>4.2.4.RELEASE</version>
	</dependency>
	<dependency>
	    <groupId>org.springframework</groupId>
	    <artifactId>spring-tx</artifactId>
	    <version>4.2.4.RELEASE</version>
	</dependency>
	<dependency>
	    <groupId>mysql</groupId>
	    <artifactId>mysql-connector-java</artifactId>
	    <version>5.1.38</version>
	</dependency>
	<dependency>
	    <groupId>commons-dbcp</groupId>
	    <artifactId>commons-dbcp</artifactId>
	    <version>1.2.2</version>
	</dependency>
	<dependency>
	    <groupId>commons-pool</groupId>
	    <artifactId>commons-pool</artifactId>
	    <version>1.5.3</version>
	</dependency>
	<dependency>
	    <groupId>com.alibaba</groupId>
	    <artifactId>druid</artifactId>
	    <version>1.0.18</version>
	</dependency>
	<dependency>
	    <groupId>c3p0</groupId>
	    <artifactId>c3p0</artifactId>
	    <version>0.9.1.2</version>
	</dependency>
  	<dependency>
	    <groupId>cglib</groupId>
	    <artifactId>cglib</artifactId>
	    <version>2.2.2</version>
	</dependency>
  	<dependency>
	    <groupId>org.mybatis</groupId>
	    <artifactId>mybatis</artifactId>
	    <version>3.2.7</version>
	</dependency>
	<dependency>
	    <groupId>org.mybatis</groupId>
	    <artifactId>mybatis-spring</artifactId>
	    <version>1.2.2</version>
	</dependency>
	<dependency>
	    <groupId>org.springframework</groupId>
	    <artifactId>spring-context-support</artifactId>
	    <version>4.2.4.RELEASE</version>
	</dependency>
  </dependencies>
```
2. 添加相关配置文件<br/>
 ```
 1.log4j.properties
 2.jdbc.properties
 3.SqlMapConfig.xml
 <!-- 只写 config和mapper标签 -->
 4.mapper.xml
 5.applicationContext.xml
 <!-- 三步  1.准备数据源 2.声明工厂类 3.将工厂类注入dao -->
 ```
3. 编写java代码
```
1.pojo
2.dao & daoImpl
3.service & serviceImpl
3.Test
```
