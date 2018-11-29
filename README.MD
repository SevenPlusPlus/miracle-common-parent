## miracle-common-parent简介

> 这是一个用于maven jar包依赖管理的pom，推荐作为dependecyManagement使用。功能类似spring-boot-dependencies,管理我们自主开发的jar包版本，解决依赖版本冲突的问题。    —— [维基百科](https://zh.wikipedia.org/wiki/Markdown)


这是spring-boot项目的一个使用示例，tips：当多个dependencyManage指定的同一jar包版本冲突时，会优先先定义的。
``` python
<dependencyManagement>
		<dependencies>
			<dependency>
				<groupId>com.melot</groupId>
				<artifactId>melot-common-dependencies</artifactId>
				<version>1.0.0</version>
				<type>pom</type>
				<scope>import</scope>
			</dependency>
			<dependency>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-dependencies</artifactId>
				<version>${springboot.version}</version>
				<type>pom</type>
				<scope>import</scope>
			</dependency>
		</dependencies>
	</dependencyManagement>
```

