
dns https://jocent.me/2017/06/18/dns-protocol-principle.html



1:标志：
qr  查询标志，0查询，1，响应
opcode  0标准查询，1，反向查询，2 服务器状态请求

aa 表示授权回答，tc表示可以阶段，rd  期望递归，ra 可用递归  rcode 返回码

questions：查询区域数量，answers表示回答区域数量，authoritative namesversers表示授权区域书
addtional recordess表示区域的数量

query区域

查询名：长度不固定，不适用填充字节

查询类型
a 域名查询ipv4地址
ns  查询域名服务器
cname 查询规范名称
soa 开始授权
wks 熟知服务
ptr 把ip地址转换成域名
hinfo 主机信息
mx 邮件交换
aaaa 由域名获取ipv6地址
axfr 传送整个区域
any  对所有记录的请求
1. 资源记录(RR)区域（包括回答区域，授权区域和附加区域）





mdns：

https://esp-idf-zh.readthedocs.io/zh_CN/latest/api-reference/protocols/mdns.html

提供网络服务和主机发现

主机名：esp.local
distance:distance

网络服务：发现其他服务

主机发现：发现其他mdns distance


1:dns查询，创建socket向组播地址查询。
2:dns响应，用socket向组播地址响应。
3:服务的请求和响应。




https://itbilu.com/other/relate/EyxzdVl3.html
#A或AAAA
分别是ipv4和ipv6的域名ip映射，将域名制定ip，相反的对应为PTR记录。
#PTR记录
1. 看A记录
2. 再mdns中，ptr代表到是将服务解析到host，是srv的相反。
#CNAME记录
域名---》域名---》ip，后面的部分是A记录

#SRV记录
添加服务记录服务器时候会添加此记录，SRV记录了哪台计算机提供了哪个服务，格式为服务名称.协议类型


#mdns协议原理 https://www.binkery.com/archives/318.html

#QM和Qu的区别
