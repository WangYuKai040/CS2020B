# 資訊工程導論
![computer](computer.jpg)
![protocol](protocol.jpg)

# OSI (Open System Interconnection Model,OSI模型)
```
1.實體層(Physical Layer):負責管理電腦通訊裝置和網路媒體之間的互通
包括了針腳、電壓、線纜規範、集線器、中繼器、網卡、主機介面卡等
2.資料連結層(Date Line Layer):負責網路尋址、錯誤偵測和改錯
例如乙太網、無線區域網路（Wi-Fi）和通用分組無線服務（GPRS）等
3.網路層(Network Layer):將網路表頭（NH）加至數據包，以形成封包
例如:網際網路協定（IP）等
4.傳輸層(Transport Layer):把傳輸表頭（TH）加至數據以形成數據包
例如:傳輸控制協定（TCP）等
5.會議層(Session Layer):負責在數據傳輸中設定和維護電腦網路中兩台電腦之間的通訊連接
6.表現層(Presentation Layer):把數據轉換為能與接收者的系統格式相容並適合傳輸的格式
7.應用層(Application Layer):提供為應用軟體而設計的介面，以設定與另一應用軟體之間的通訊
```
# MAC Address (Media Access Control Address,MAC位址)
```
也稱為區域網路位址（LAN Address），乙太網路位址（Ethernet Address）或實體位址（Physical Address）
```
```
CMD>ipconfig


Microsoft Windows [版本 6.1.7601]
Copyright (c) 2009 Microsoft Corporation.  All rights reserved.

C:\Users\User>ipconfig

Windows IP 設定


乙太網路卡 區域連線:

   連線特定 DNS 尾碼 . . . . . . . . : ksu.edu.tw
   連結-本機 IPv6 位址 . . . . . . . : fe80::a8ab:57f2:202f:41e7%11
   IPv4 位址 . . . . . . . . . . . . : 120.114.137.164
   子網路遮罩 . . . . . . . . . . . .: 255.255.255.192
   預設閘道 . . . . . . . . . . . . .: 120.114.137.190

通道介面卡 6TO4 Adapter:

   連線特定 DNS 尾碼 . . . . . . . . : ksu.edu.tw
   IPv6 位址. . . . . . . . . . . . .: 2002:7872:89a4::7872:89a4
   預設閘道 . . . . . . . . . . . . .:

通道介面卡 isatap.ksu.edu.tw:

   媒體狀態 . . . . . . . . . . . . .: 媒體已中斷連線
   連線特定 DNS 尾碼 . . . . . . . . : ksu.edu.tw

C:\Users\User>
```
# IP (Internet Protocol,網際網路協定)
```
IP是在TCP/IP協定套組中網路層的主要協定
第一個架構的主要版本為IPv4，目前仍廣泛使用，儘管世界各地正在積極部署IPv6
```
# PORT (通訊埠)
```
又稱為連接埠、埠、協定埠（protocol port）
```
```
在一個電腦作業系統中扮演通訊的端點（endpoint）。每個通訊埠都會與主機的IP位址及通訊協定關聯。通訊埠以16位元數字來表示，這被稱為通訊埠編號（port number）
```
# UDP (User Datagram Protocol,UDP 用戶資料報協定) 
```
不可靠,不穩定,但快
```
# TCP (Transmission Control Protocol,TCP 傳輸控制協定) 
```
可靠,穩定,但慢
```
```
是一種連接導向的、可靠的、基於位元組流的傳輸層通信協定，由IETF的RFC 793定義
在簡化的電腦網路OSI模型中，它完成第四層傳輸層所指定的功能。用戶資料報協定（UDP）是同一層內另一個重要的傳輸協定
```
# Three-way Handshake(三項交握)
```
其建立虛擬連線 (virtual connection) 的方式。
又稱為 三向式握手、三路交握 …，其實就是 三次訊息的交換。
```
# TCP/IP(TCP/IP Protocol Suite,TCP/IP協定套組)
```又被稱為TCP/IP協定疊（英語：TCP/IP Protocol Stack）
https://zh.wikipedia.org/wiki/TCP/IP%E5%8D%8F%E8%AE%AE%E6%97%8F
```
```
TCP/IP提供了點對點連結的機制，將資料應該如何封裝、定址、傳輸、路由以及在目的地如何接收，都加以標準化。它將軟體通訊過程抽象化為四個抽象層
```
# 不同電腦執行的不同協定
```
一個簡單的路由器上可能會實現ARP，IP，ICMP，UDP，SNMP，RIP。
WWW用戶端使用ARP，IP，ICMP，UDP，TCP，DNS，HTTP，FTP。
一台用戶電腦上還會執行如TELNET，SMTP，POP3，SNMP，ECHO，DHCP，SSH，NNTP。
無盤裝置可能會在韌體，比如ROM中實現ARP，IP，ICMP，UDP，BOOTP，TFTP（均為面向封包的協定，實現起來相對簡單）。
```
# 連接埠口
```
21 FTP ，檔案傳輸協定的命令通道。
22 SSH ，較為安全的遠端連線伺服器。
23 Telnet ，早期的遠端伺服器連線軟體。
80 WWW ， 全球資訊網伺服器。
110 POP3 ，郵件收信協定，辦公室用的收信軟體都靠它。
443 https ， 有安全加密機制的WWW伺服器。
HTTP也是有加密的機制，使用SSL ( Security Socket Layer ) 對HTTP加密形成 https (http over SSL ) 當你發現目前你所在的網頁一開始的協定是https而不是http時，表示你正在瀏覽加密過的網頁。
```
