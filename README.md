# py_socket
用python写的socket server，采用非阻塞的方式，使用epoll I/O模型。消息经server发给redis入队列后由守护进程转发到各个web机上由php编写的程序进行数据处理，产生结果后塞入redis的通道。socket server订阅该通道得到消息后返回给等待的客户端连接。
