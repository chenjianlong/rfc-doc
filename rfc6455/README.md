# RFC-6455 WebSocket 协议翻译

* 原文：[The WebSocket Protocol](http://tools.ietf.org/html/rfc6455)
* 翻译：[websocket协议翻译](https://github.com/zhangkaitao/websocket-protocol)

## 摘要

WebSocket 协议实现在受控环境中运行不受信任代码的一个客户端到一个从该代码已经选择加入通信的远程主机之间的全双工通信。
用于这个的安全模型是通常由 web 浏览器使用的基于来源的安全模型。
该协议包括一个打开阶段握手、接着是基本消息帧、TCP之上的分层（layered over TCP）。
该技术的目标是为需要与服务器全双工通信且不需要依赖打开多个HTTP连接
（例如，使用 XMLHttpRequest 或 < iframe \> 和长轮询）的基于浏览器应用的提供一种机制。

## 本备忘录状态

这是一个Internet标准跟踪文档。

本文档是互联网工程任务组（IETF）的一个产物。
它代表了IETF社区的共识。
它已接受公共审查和已经被互联网工程指导委员会（IESG）认可发布。
Internet标准的更多信息可在 [RFC 5741第2节](http://tools.ietf.org/html/rfc5741#section-2) 找到。

本文档的当前状态信息、任何勘误表以及如何提供它的反馈，可于 http://www.rfc-editor.org/info/rfc6455 获取。

## 版权声明

版权所有（C） 2011 IETF信托和确认为文档作者的人。
保留所有权利。

本文档遵守BCP 78和涉及IETF文档 (http://trustee.ietf.org/license-info) 的在本文档发布之日起生效的IETF信托的法律条文。
请仔细阅读这些文档，因为他们描述了关于本文档的你的权利和限制。
从本文档中提取的代码组件必须包括描述在第四章的简体BSD License文件。
e的信托法律条文并提供，不保证描述在简体BSD License中。

