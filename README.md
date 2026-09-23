# frp_pyd

user pyd remote any computer or server 


如何使用？

在pyd文件所在的目录下，使用cmd命令调用（内存占用极小）：

1.提供远程的服务端：
python -c "import asyncio,frps;asyncio.run(frps.main('0.0.0.0',8800,'0.0.0.0',8801))"

2.被远程的客户端：
python -c "import asyncio,frpc;asyncio.run(frpc.main('124.221.146.69',8800,'localhost',3389))"

3.发起远程的电脑：124.221.146.69:8801

4.python版本：3.14.X（X86-64、AMD）



