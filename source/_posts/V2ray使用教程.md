---
title: V2ray使用教程
category: 
renderNumberedHeading: true
grammar_cjkRuby: true
tags: 'v2ray,教程,说明'
cover_picture: https://img.aavf.cn/img/dhuadanfl22.png
---



 - 首先. 进入解压后的V2rayN-core目录，双击”v2rayN”文件，程序启动后会最小化到右下角的托盘(桌面右下角，显示时间输入法那块)。双击蓝色的V字小图标，打开V2rayN的主界面：
![enter description here](https://img.aavf.cn/img/dhuadanfl22.png)
 

- 接着添加新的V2ray节点：点击界面上方的“服务器”，按照自己节点类型选择，注意VMess服务器和VLESS服务器是不同的！
![enter description here](https://img.aavf.cn/img/202004201523.png)

- 这里以我们以手动VLESS服务器为例进行说明，根据V2ray节点信息填写地址、端口、用户ID等、流控等信息。VLESS协议不需要额外id（alterID），所以不需要填写。反过来说如果你看到要填写额外ID，说明服务器类型选错了！

- 配置好后点击确定，主界面出现了节点的简要信息。可以双击节点那一行再次出来上面的配置界面修改配置，也可以点击右键删除、移动该节点：

- 配置好节点后需要设置系统代理才能让浏览器访问外网，操作为：右下角托盘找到v2rayN图
标，在图标上点击右键，找到“系统代理” ，点击“自动配置系统代理”，此时图标会变成红色：
![](https://img.aavf.cn/img/202204201528.png)