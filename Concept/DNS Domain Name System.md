# DNS(Domain Name System)

Created: Feb 21, 2020 6:40 PM
Tags: TCP/IP, 域名, 网络

### 域名系统

域名系统（Domain Name System缩写DNS，Domain Name被译为域名）是因特网的一项核心服务，它作为可以将域名和IP地址相互映射的一个分布式数据库，能够使人更方便的访问互联网，而不用去记住能够被机器直接读取的IP数串。

域名系统(Domain Name System,DNS)是Internet上解决网上机器命名的一种系统。就像拜访朋友要先知道别人家怎么走一样，Internet上当一台主机要访问另外一台主机时，必须首先获知其地址，TCP/IP中的IP地址是由四段以“.”分开的数字组成，记起来总是不如名字那么方便，所以，就采用了域名系统来管理名字和IP的对应关系。

## **DNS 解锁原理**

**首先你需要有一台能看 Netflix 或者其它流媒体的服务器，用作DNS服务器和HTTPS代理。**

DNS 解锁服务器主要起到两个作用：

1. 提供 DNS 解析，将符合流媒体的域名解析到自己的IP
2. 解析到自己的 IP 后提供[HTTPS/HTTP](https://www.notion.so/HTTP-HTTPS-432a7b142363403ea2f6baf72e4f31c4)的代理（SNIProxy）这样就能代理访问流媒体了。

大致的原理和流程可以参考下图：

![https://fx.tmioe.com/wp-content/uploads/2019/11/1574310187-01.png](https://fx.tmioe.com/wp-content/uploads/2019/11/1574310187-01.png)