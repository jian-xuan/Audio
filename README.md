# 概述
用于共享一个PC收集到的麦克风声音到另一台PC上播放，主要运用java和netty实现
# 使用
1. 在target里有生成好的jar包，可直接使用
2. 服务端直接启动
3. 客户端需要先在jar包里的application.properties 中指定服务端的ip地址，不然无法连接
# 根据需求已经实现的功能
- 无需先启动服务端，就算是客户端先启动，也能连接上。
- 基于netty的断开重连实现，断开后，会恢复监听端口模式，无论是客户端还是服务端断开，都可以在不重启另一端的情况下进行连接
- 客户端连接无超时，方便服务端意外关闭较长时间而需重新连接的情况
