# 小米路由器web端添加指示灯开关功能
## MIRouter-Indicator-Light-Control
自学web前端开发，目前做了个小demo出来

使用方法
---

1. 浏览器安装油猴(Tampermonkey)扩展程序，打开油猴，新建脚本，然后将代码复制进去，或者前往[脚本安装界面](https://greasyfork.org/zh-CN/scripts/407039)
2. 更改`// @match  http://192.168.31.1/cgi-bin/luci/;stok=*` 将 `192.168.31.1`替换为自己路由器的地址，或者访问`miwifi.com` 进入web管理页面
3. 打开web端并登陆，脚本将在web端添加如下灯泡
   <img src='./image/led_on.png'  width = '200px'>
4. 点击灯泡即可关闭效果如下图所示
   <img src='./image/led_off.png'  width = '200px'>
5. 总体效果
   <img src='./image/led.gif'>
6. 通知显示效果  
   //TODO

版本记录
---
`v0.2.3` 引用 [Notyf](https://github.com/caroso1222/notyf) 加入了通知功能  
`v0.2.2` 修正URL硬编码 bug   
`v0.2.1` 初始功能完成


PS:
---
+ 脚本默认最大点击次数为5次，超过之后将禁用，刷新页面后恢复，如需更改请自行修改源代码
+ 仅在macOS Catalina 以及 Chrome 83.0.4103.116（正式版本）下测试无问题，其他环境请自行验证

开关灯的建议实现
---
1. 登录路由器web端，在地址栏链接中提取token，地址栏链接结构为 `http://miwifi.com/cgi-bin/luci/;stok={32位字符串}/web/home#router`
2. 请求下述地址即可实现开启与关闭状态指示灯：  
开灯： 
`http://192.168.31.1/cgi-bin/luci/;stok={token}/api/misystem/led?on=1`  
关灯：
`http://192.168.31.1/cgi-bin/luci/;stok={token}/api/misystem/led?on=0`  




参考链接
---
[灯泡css来源](https://www.jq22.com/code963)



