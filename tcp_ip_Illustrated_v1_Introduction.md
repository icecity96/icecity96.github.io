## 概述

### TCP/IP模型基本分层及其功能

| layers 		| protocols 				|
|--------		|-----------				|
| Application	| Telent,Ftp,Email,etc	|
| Transport	| TCP,UDP					|
| Network		| IP,ICMP,IGMP			|
| Link			| device driver and interface card|

* **Link**(链路层):有时也被称为**data-link**(数据链路层)或**network interface**(网络接口层通常包括操作系统中的设备驱动程序和计算机中对应的网络接口卡.
* **NetWork**(网络层):主要用来处理Packet在网络中的活动
* **Transport**(传输层):为两台主机上的应用程序提供端到端的通信
* **Application**(应用层):负责处理特定的应用程序细节

### End-to-End && Hop-by-Hop
* **End-to-End**(端到端):Application layer 和 Transport layer 使用end-to-end协议，即只有在**End system**(端系统)才需要的协议
* **Hop-by-hop**(逐跳): 端系统和中间系统都需要使用

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTVlsErZMe9rC4ct-Slq950MoUcMaVnxQm9AsGJlrd94tf-ZHw5UQ)

### 不可靠服务与可靠服务
* **不可靠服务**:尽最大努力交付，并**不做任何保证**,如IP，UDP
* **可靠服务**:保证不错，不丢，不乱，如TCP采用超时重传，确认分组等机制保障可靠服务。

### IP地址
* 作用:用于标识网络上一个终端的身份
* IP地址的分类:
 
| Class | Range |
| ------|-------|
|A|0.0.0.0 to 127.255.255.255|
|B|128.0.0.0 to 191.255.255.255|
|C|192.0.0.0 to 223.255.255.255|
|D|224.0.0.0 to 239.255.255.255|
|E|240.0.0.0 to 247.255.255.255|

### 封装与解封
![封装](http://img.voidcn.com/vcimg/000/004/876/112_ebd_4ed.png)

### 端口号
* 作用:用于标识一个主机内的进程
* 分类:
	* 熟知端口
	* 动态端口
	* 保留端口