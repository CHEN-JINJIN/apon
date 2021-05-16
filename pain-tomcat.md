# Apache Tomcat

The Apache Tomcat® software is an open source implementation of the Jakarta Servlet, Jakarta Server Pages, Jakarta Expression Language, Jakarta WebSocket, Jakarta Annotations and Jakarta Authentication specifications. These specifications are part of the Jakarta EE platform.

The Jakarta EE platform is the evolution of the Java EE platform. Tomcat 10 and later implement specifications developed as part of Jakarta EE. Tomcat 9 and earlier implement specifications developed as part of Java EE.

The Apache Tomcat software is developed in an open and participatory environment and released under the Apache License version 2. The Apache Tomcat project is intended to be a collaboration of the best-of-breed developers from around the world. We invite you to participate in this open development project. To learn more about getting involved, [click here](https://tomcat.apache.org/getinvolved.html).

Apache Tomcat software powers numerous large-scale, mission-critical web applications across a diverse range of industries and organizations. Some of these users and their stories are listed on the PoweredBy wiki page.

Apache Tomcat, Tomcat, Apache, the Apache feather, and the Apache Tomcat project logo are trademarks of the Apache Software Foundation.

<details>
<summary>（点击）查看翻译</summary>

Apache Tomcat®软件是Jakarta Servlet、Jakarta Server Pages、Jakarta Expression Language、Jakarta WebSocket、Jakarta Annotations和Jakarta Authentication specification的开源实现。这些规范是Jakarta EE平台的一部分。

Jakarta EE平台是Java EE平台的演变。Tomcat 10以及以后的实现规范作为Jakarta EE的一部分开发。Tomcat 9和早期的实现规范是作为Java EE的一部分开发的。

Apache Tomcat软件是在一个开放和参与的环境中开发的，并在Apache许可证版本2下发布。Apache Tomcat项目旨在成为来自世界各地的最佳开发人员的协作。我们邀请您参与这个开放开发项目。想了解更多关于参与的信息，[请点击这里](https://tomcat.apache.org/getinvolved.html)。

Apache Tomcat软件支持许多跨不同行业和组织的大规模、关键任务的web应用程序。PoweredBy wiki页面列出了其中一些用户及其故事。

Apache Tomcat、Tomcat、Apache、Apache羽毛和Apache Tomcat项目标志都是Apache软件基金会的商标。
</details>

## Download

[Tomcat8](http://tomcat.apache.org/download-80.cgi) 最新官网下载地址：[http://tomcat.apache.org/download-80.cgi](http://tomcat.apache.org/download-80.cgi)

?>目前`iPainfree`系统推荐使用Tomcat8

## Tomcat配置

- 启动模式（`Startup type`）：`Automatic`（开机自启）
- 禁止auto打印Stdout日志（防止stdout.log文件暴增）
- 设置tomcat端口&URI字符集为`utf-8`，配置文件`./conf/server.xml`

```xml
<Connector port="8080" protocol="HTTP/1.1"
               connectionTimeout="20000" URIEncoding="utf-8"
               redirectPort="8443" />
```


## Tomcat注意事项

