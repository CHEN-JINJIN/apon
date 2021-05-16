# JDK

`JDK`是 Java 语言的软件开发工具包，主要用于移动设备、嵌入式设备上的java应用程序。JDK是整个java开发的核心，它包含了JAVA的运行环境（JVM+Java系统类库）和JAVA工具。

## Download

[JDK8](https://www.oracle.com/cn/java/technologies/javase/javase-jdk8-downloads.html) 最新官网下载地址：[https://www.oracle.com/cn/java/technologies/javase/javase-jdk8-downloads.html](https://www.oracle.com/cn/java/technologies/javase/javase-jdk8-downloads.html)

?>目前`iPainfree`系统推荐使用JDK8

## JDK环境变量配置

| 变量名             | 变量值                                               |
|-----------------|---------------------------------------------------|
| `JAVA_HOME` （需新建） | JDK安装后所在路径 （如：C:\Program Files\Java\jdk1.8.0_102） |
| `Path`            | ;`%JAVA_HOME%\bin`                                  |


## JDK环境配置验证

```java
javac -version
```

