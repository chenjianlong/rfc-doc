# 12. 在其他规范中使用 WebSocket 协议

WebSocket协议目的是被其他规范使用来提供一个通用机制来动态作者定义内容，例如，在一个规范中定义一个脚本API。

这样的规范首先需要 \_建议一个WebSocket连接\_，该算法是：

*  目的地，包含一个/host/和一个/port/。
*  一个/resource name/，允许在一个 host 和 port 标识多个服务。
*  一个/secure/标记，如果连接是加密的则为true，否则为false。
*  一个源[[RFC6454](http://tools.ietf.org/html/rfc6454)]的ASCII序列化，负责连接。
*  可选的， 一个字符串标识一个协议，层叠在 WebSocket 连接之上。

/host/、/port/、/resource name/ 和/secure/标记通常从一个URI中使用该步骤解析一个WebSocketURI组件获得。
如果没有指定一个WebSocket，则这些步骤失败。

如果在任何时候连接将被关闭，那么规范需要使用 \_关闭WebSocket连接\_ 算法（[7.1.1节](http://tools.ietf.org/html/rfc6455#section-7.1.1)）。

[7.1.4节](http://tools.ietf.org/html/rfc6455#section-7.1.4)定义了什么时候 \_WebSocket连接关闭\_ 。

当打开一个连接，规范将需要处理什么时候 \_已经接收了一个WebSocket消息\_ 的情况（[6.2节](http://tools.ietf.org/html/rfc6455#section-6.2)）。

要发送一些数据/data/到一个打开的连接，规范需要 \_发送一个WebSocket消息\_（[6.1节](http://tools.ietf.org/html/rfc6455#section-6.1)）。
