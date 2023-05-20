# CHN-CT 广州家宽 VoWiFi 启用教程  

以Pixel7Pro为案例,pixel6-7应完美适配 pixel系列关键字句应相同 类原生可参考  

1.打开 VoWiFi 开关
2.使用 Adb 链接设备 查看Logcat 关键字句: `EpdgTunnelManager`  
3.未出现`Closing tunnel with exception`之类的字句的情况下  
4.字句 `Ike session opened for apn: ims with token` 为IPSec通道建立成功  
5.打开飞行模式 测试  
6.enjoy VoWiFi  

note1: 寻找字段`Valid ePDG Address List`,他们为VoWifi服务的ip表 按需求白名单/黑名单
note2: `EpdgTunnelManager[]`后的括号内数字为sim卡序号 不同卡的epdg服务是分开的
note3: `IWLAN_IKE_INTERNAL_IO_EXCEPTION`一般为被服务器拒绝了的原因 详情请google
note4: 已知epdg服务ip将在ims_ePDG文件夹内以运营商名列出

see <https://www.arubanetworks.com/techdocs/Instant_87_WebHelp/Content/instant-ug/voice-and-video/wifi-calling.htm>

Copyright © 2023 QueallyTech, All Rights Reserved.