## http1 http2 的区别

http1 报文是文本 http2 报文是二进制
按照报文大小分成了不同的帧
引入了 帧(frame)和流(stream)的概念

帧是按照报文段分割，分割成每一小块，每一小块呗成为一个帧
流是通过帧的首部来标识的
有了帧和流的引入就可以实现多路复用

可以在传输中有很多流的产生，可任意发送请求和响应 不限制数量

因为不限制数量就不会产生对头阻塞问题

serverPush 服务端推送，服务端可以向客户端主动推送一些资源

优先级

永久链接
