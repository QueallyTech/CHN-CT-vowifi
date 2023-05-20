# CHN-CT 广州家宽 VoWiFi 启用教程  

教程编写不易 欢迎star与提交您运营商的ePDG ip  
教程偏技术 由于该功能暂试点 只能提供如何确认当前是否满足开启条件 无法提供云端的服务规则  

## 如何确认是否满足条件

以 Pixel7Pro 为案例,Pixel6-7 系列应完美适配,Pixel系列设备关键字句应相同,类原生可参考  

1. 打开 VoWiFi 开关
2. 使用 Adb 链接设备 查看Logcat 关键字句: `EpdgTunnelManager`  
3. 未出现`Closing tunnel with exception`之类的字句的情况下  
4. 字句 `Ike session opened for apn: ims with token` 为IPSec通道建立成功  
5. 打开飞行模式 测试  
6. enjoy VoWiFi  

## my case的网络条件

1. 电信家宽(与手机号实名相同 且好像为融合套餐)
2. 使用 光猫桥接与路由器拨号 拥有非固定的公网IP

## 注

1. 寻找字段`Valid ePDG Address List`,他们为VoWifi服务的ip表 按需求白名单/黑名单  
2. `EpdgTunnelManager[]`后的括号内数字为sim卡序号 不同卡的epdg服务是分开的  
3. `IWLAN_IKE_INTERNAL_IO_EXCEPTION`一般为被服务器拒绝了的原因 详情请google  
4. 已知ePDG服务ip将在本repo的`ims_ePDG`文件夹内以运营商信息列出  
5. 建议将ePDG服务ip扔进白名单以免未知错误

see <https://www.arubanetworks.com/techdocs/Instant_87_WebHelp/Content/instant-ug/voice-and-video/wifi-calling.htm>

转载请附上本文链接  
Copyright © 2023 QueallyTech, All Rights Reserved.
