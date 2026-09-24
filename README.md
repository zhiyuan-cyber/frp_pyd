# frp_pyd（Python版 frp 实现远程穿透）

use frp pyd remote any computers or servers 


如何使用？

在pyd文件所在的目录下，使用cmd命令调用：


1.提供远程的服务端（目录下得有frps.pyd），cmd输入：


python -c "import asyncio,frps;asyncio.run(frps.main('0.0.0.0',8800,'0.0.0.0',8801))"


2.被远程的客户端（目录下得有frpc.pyd）（假设提供远程的服务端IP为：124.221.146.69），cmd输入：


python -c "import asyncio,frpc;asyncio.run(frpc.main('124.221.146.69',8800,'localhost',3389))"


3.发起远程的电脑：

用微软的rdp（远程桌面软件）输入:

124.221.146.69:8801

完成访问


4.python版本：3.14.X（X86-64、AMD）


5.已经实现前后端断线重连功能，服务端支持异常捕获处理，客户端支持重连。


6.目前已支持多端口服务，一台服务器可以提供多个远程服务，可开服。


7.60fps注册表方便实现远程桌面达到60帧，方便快捷。


8.后续计划：

①开源完整代码和编译脚本。

②优化UDP协议支持。

③目前客户端占用内存仅有10MB，服务端占用内存仅10MB，在内存价格飞涨的今天，将持续优化程序，以轻便化的姿态降低内存使用量。


