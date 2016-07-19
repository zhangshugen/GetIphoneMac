# GetIphoneMac
该工程主要应用于获取苹果手机的mac地址，但前提是连接了wifi路由的情况下。原理：我们知道苹果是不允许我们获取其设备硬件的mac地址的，在iOS7以下才可以获得。iOS7以后苹果对于sysctl和ioctl进行了技术处理，MAC地址返回的都是02:00:00:00:00:00。但是发现fing这个软件却可以获取，其下载地址为：https://appsto.re/cn/tw1Rz.i  相关讨论地址：http://stackoverflow.com/questions/27099108/how-does-ios-app-fing-get-mac-address 。发现是基于arp来和路由器交互然后获取当前路由器下的缓存设备表，然后我们就可以根据ip来判断本机mac地址了。但是我发现这个缓存表数据时多时少，很难找全，但fing却可以。所以希望靠大家的力量一起来研究分享！
#例子效果图
![](https://github.com/Jdb156158/GetIphoneMac/blob/master/FC0EB9F3-DF61-4DF2-86E1-381AE3E87134.png)