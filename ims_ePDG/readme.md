# ims_eDPG

该文件夹存有运营商的 `ePDG` 服务器ip与域名,可能随着时间变化存在变动  
欢迎提交pr完善该目录  
命名规则: `MCC-MNC_服务提供商-运营商-地区`  
如: `454(NCC)-0(MNC)_CSL(服务提供商)-CLUB(运营商)-香港(地区)`
若服务提供商或运营商存在 `-` 使用 `_` 替换,请使用utf-8格式编码储存

## 获取 ePDG 服务分发网址

以 Pixel7Pro 为案例,Pixel6-7 系列应完美适配,Pixel系列设备关键字句应相同,类原生可参考  

设备Logcat中 由`EpdgSelector` 发送的 `Input domainName`  
logcat内域名即为ePDG服务请求域名  

部分运营商将使用标准 FQDN 格式的ePDG请求域名,请确保该域名能被正确解析以获取ip列表  
标准格式请求的域名将可能在漫游下 因使用正在连接网络的 MNC与MCC 发送请求 而无法正常请求到结果  
若出现该情况 尝试请使用 `iwlan.epdg_static_address_string` 字段 手动设置  

## 获取ePDG ip列表

以 Pixel7Pro 为案例,Pixel6-7 系列应完美适配,Pixel系列设备关键字句应相同,类原生可参考  

设备Logcat中 由`EpdgTunnelManager[]` 发送的 `Valid ePDG Address List:`  
列表内ip即为ePDG服务器ip