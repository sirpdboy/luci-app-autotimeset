luci-app-autopoweroff for OpenWRT/Lede(中文)
源码地址 https://github.com/sirpdboy/luci-app-autopoweroff

定时重启关机1.3 二合一升级版,你可以免费使用代码，但请注明出处。
彻底解决需要保存二次才生效的问题。

Install to OpenWRT/LEDE


git clone https://github.com/sirpdboy/luci-app-autopoweroff

cp -r luci-app-autopoweroff LEDE_DIR/package/luci-app-autopoweroff


cd LEDE_DIR

./scripts/feeds update -a

./scripts/feeds install -a


make menuconfig

LuCI  --->

	1. Collections  --->
	
		<*> luci
		
	3. Applications  --->
	
		<*> luci-app-autopoweroff.........................LuCI support for Scheduled poweroff
		
make package/luci-app-autopoweroff/compile V=s
