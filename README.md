# dubboss

一个分布式REST服务的框架,实现了如下功能:

+   基于dubbo的RPC
+   基于netty的应用服务器
+   基于springmvc的REST调用
+   基于ngnix的负载均衡

#### 如何快速使用

1.  启动服务提供者: cn.injava.dubboss.service.starter.StartService
2.  启动服务调用着: cn.injava.dubboss.server.starter.StartServer
3.  通过浏览器访问 http://localhost:8080/hello/dubboss, 如果返回Hello开头的信息,表示REST调用成功

#### 如何打包并部署

1.  在根目录下执行maven打包命令: mvn package
2.  启动服务提供着: java -jar dubboss-server/target/dubboss-server-1.0-SNAPSHOT.jar
3.  启动服务调用着: java -jar dubboss-service/target/dubboss-service-1.0-SNAPSHOT.jar
4.  通过浏览器访问 http://localhost:8080/hello/dubboss, 如果返回Hello开头的信息,表示REST调用成功

#### TODO

+   参考dubbo的SpringContainer类,在starter里提供停止服务的方法
+   实现session共享
+   后台启动的脚本
+   接入数据库,以及数据库中间件