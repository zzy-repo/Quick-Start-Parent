# Quick-Start-Parent
## 概述
Quick-Start-Parent 是一个基于 Maven 的依赖管理（BOM）文件，用于快速启动一个新项目。

该项目包含了一系列常用依赖的版本管理，以便于在创建新项目时能够快速集成所需的库。

## 依赖列表
以下是一些本项目管理的依赖：
- Spring Boot
- Lombok
- MySQL Connector/J
- MyBatis-Plus
- Java JWT
- JUnit Jupiter
- Velocity Engine
- SLF4J
- Hutool
- SpringDoc OpenAPI
- Druid
- Shiro

## 使用方法
1. **添加到本地仓库**:
   在将 Quick-Start-Parent 项目作为依赖管理之前，需要将其安装到您的本地 Maven 仓库。执行以下命令来安装：
   
   ```bash
   mvn install
   ```
   这将在本地 Maven 仓库中安装 Quick-Start-Parent。
2. **在您的 Maven 项目中添加依赖管理**:
   将以下内容添加到 `pom.xml` 文件的 `<dependencyManagement>` 部分：
   
   ```xml
   <dependencyManagement>
       <dependencies>
           <dependency>
               <groupId>me.zzy</groupId>
               <artifactId>Quick-Start-Parent</artifactId>
               <version>1.0-SNAPSHOT</version>
               <type>pom</type>
               <scope>import</scope>
           </dependency>
       </dependencies>
   </dependencyManagement>
   ```
3. **添加依赖**:
   在您项目的 `<dependencies>` 部分添加具体的依赖，例如：
   ```xml
   <dependencies>
       <!-- Spring Boot Starter Web -->
       <dependency>
           <groupId>org.springframework.boot</groupId>
           <artifactId>spring-boot-starter-web</artifactId>
       </dependency>
       <!-- 其他依赖 -->
   </dependencies>
   ```
   通过这种方式，将能够使用 Quick-Start-Parent 中定义的依赖版本，而无需在自己的项目中指定版本号。

