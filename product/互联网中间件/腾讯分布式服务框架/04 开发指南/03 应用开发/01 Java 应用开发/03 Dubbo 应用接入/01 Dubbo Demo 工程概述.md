## 获取 Demo
本 Demo 工程基于 Alibaba Dubbo 版本 SDK 开发，下载地址：[Demo 下载](https://tsf-doc-attachment-1300555551.cos.ap-guangzhou.myqcloud.com/demo/dubbo/tsf-dubbo-alibaba-demo-1.1.7.zip) 。

>?
>- 本 Demo 工程仅是示例，现存的 Dubbo 应用接入 TSF 可以直接参见 [Dubbo 应用接入TSF](https://cloud.tencent.com/document/product/649/13947)。
>- 如果从零开始新开发的微服务系统推荐采用 Spring Cloud 框架，详情参见 [Spring Cloud TSF 应用开发](https://cloud.tencent.com/document/product/649/74249)。

## 工程目录
`tsf-dubbo-xxx-demo`的工程目录如下：

```
|- consumer-demo
|- provider-demo
|- pom.xml
```
其中 consumer-demo 表示服务消费者， provider-demo 表示服务提供者，pom.xml 中定义了工程需要的依赖包：
<dx-codeblock>
:::  xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.1.3.RELEASE</version>
    </parent>

    <artifactId>provider-demo</artifactId>
    <version>1.1.7-alibaba-RELEASE</version>
    <packaging>jar</packaging>
    <name>provider-demo</name>

    <properties>
        <start-class>com.tsf.demo.provider.ProviderApplication</start-class>
    </properties>

    <dependencies>
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <version>1.18.6</version>
            <scope>provided</scope>
        </dependency>
        <dependency>
            <groupId>com.tencent.tsf</groupId>
            <artifactId>tsf-dubbo-registry</artifactId>
            <!-- 调整为 SDK 最新版本号 -->
            <version>1.1.7-alibaba-RELEASE</version>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
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
:::
</dx-codeblock>


