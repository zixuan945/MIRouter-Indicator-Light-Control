# MIRouter-Indicator-Light-Control
## 小米路由器web端添加指示灯开关功能

自学web前端开发，目前做了个小demo出来

### *使用方法*

1. 浏览器安装油猴(Tampermonkey)扩展程序，打开油猴，新建脚本，然后将代码复制进去
2. 更改`// @match        http://192.168.31.1/cgi-bin/luci/;stok=*` 将 `192.168.31.1`替换为自己路由器的地址
3. 打开web端并登陆，脚本将在web端添加如下灯泡
<img src='./image/led_on.png'  width = '200px'>
4. 点击灯泡即可关闭效果如下图所示
<img src='./image/led_off.png'  width = '200px'>

PS:
+ 脚本默认最大点击次数为5次，超过之后将禁用，刷新页面后恢复，如需更改请自行修改源代码
+ 仅在macOS Catalina 以及 Chrome 83.0.4103.116（正式版本）下测试无问题，其他环境请自行验证





