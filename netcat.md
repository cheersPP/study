#netcat-nc
连接和重定向套接字(Concatenate and redirect sockets)

###连接模式/监听模式：
连接模式应该就是不停发送数据，监听模式应该就是不发送数据，还有特殊的其他模式，如HTTP代理服务器模式．
在连接模式下，ncat作为客户端，在监听模式下，ncat作为服务器．

###telnet/获取banner
作用：远程服务，
命令：nc -vn IP port（可nc -h查看其他选项）
补充：-v 详细输出 -n不进行DNS解析
举例：远程登陆pop3邮箱（注意先获取IP，原因是nc解析域名速度慢），即可远程收发邮件。
![这里写图片描述](http://img.blog.csdn.net/20171109004401422?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvUDIwMTcxMTg=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

###传输文本信息
作用：电子审计
命令：服务器端 nc -l -p port
         客户端 nc -vn 服务器IP 服务器开放port
补充：-l listen侦听 -p指定端口
举例：查看可疑进程
![这里写图片描述](http://img.blog.csdn.net/20171109010052747?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvUDIwMTcxMTg=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)