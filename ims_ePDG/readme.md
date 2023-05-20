# ims_eDPG

该文件夹存有运营商的 `ePDG` 服务器ip,可能随着时间变化存在变动  
欢迎提交pr完善该目录  
命名规则: `MCC-MNC_服务提供商-运营商-地区`  
如: `454(NCC)-0(MNC)_CSL(服务提供商)-CLUB(运营商)-香港(地区)`
若服务提供商或运营商存在 `-` 使用 `_` 替换,请使用utf-8格式编码储存

## 获取ePDG ip列表

以 Pixel7Pro 为案例,Pixel6-7 系列应完美适配,Pixel系列设备关键字句应相同,类原生可参考  

设备Logcat中 由`EpdgTunnelManager[]` 发送的 `Valid ePDG Address List:`  
列表内ip即为ePDGip
