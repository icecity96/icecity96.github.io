## Ethernet && IEEE 802
* 两种封装IP的方式:**RFC 894(Ehernet)**, **RFC 1042(IEEE 802)**
* Host Requirement RFC 要求每台互联网上的主机都与一个10Mb/s的以太电缆相连接:
	* 必须能够接受和发送使用**RFC 894**封装格式的分组
	* 应该能接受与**RFC 894**混合的**RFC 1042**封装格式的分组
	* 也许能够发送**RFC 1042**格式封装的分组，如果能同时发送两种类型的分组数据那么分组应当是能设置的，且默认格式是**RFC 894**
* 两种封装格式:

![Ethernet && IEEE 802](http://telescript.denayer.wenk.be/~hcr/cn/idoceo/images/ethernet_encap.gif)

* 源地址和目的地址都使用6-byte(802.3中允许使用2-byte来表示，但一般还是使用6-byte)
* IEEE 802 中len 占用2bytes,表示其后有多少位数据(不包括CRC).Ethernet中的type表示的数据的类型。【这两者合法值是不同的】

## SLIP(串行线路IP)


