![Shadowsocks](https://github.com/teddysun/shadowsocks_install/raw/master/shadowsocks.png)
# Auto install Shadowsocks Server

shadowsocks.sh
===============
- Auto Install Shadowsocks(Python) Server for CentOS/Debian/Ubuntu
- https://teddysun.com/342.html

安装：
```
wget --no-check-certificate -O shadowsocks.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks.sh
chmod +x shadowsocks.sh
./shadowsocks.sh 2>&1 | tee shadowsocks.log
```

卸载：
```
./shadowsocks.sh uninstall
```

shadowsocks-libev.sh
===============
- Auto Install Shadowsocks(libev) Server for CentOS
- https://teddysun.com/357.html

安装：
```
wget --no-check-certificate -O shadowsocks-libev.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-libev.sh
chmod +x shadowsocks-libev.sh
./shadowsocks-libev.sh 2>&1 | tee shadowsocks-libev.log
```
卸载：
```
./shadowsocks-libev.sh uninstall
```

shadowsocks-libev-debian.sh
===============
- Auto Install Shadowsocks(libev) Server for Debian/Ubuntu
- https://teddysun.com/358.html

安装：
```
wget --no-check-certificate -O shadowsocks-libev-debian.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-libev-debian.sh
chmod +x shadowsocks-libev-debian.sh
./shadowsocks-libev-debian.sh 2>&1 | tee shadowsocks-libev-debian.log
```

卸载：
```
./shadowsocks-libev-debian.sh uninstall

```

shadowsocks-go.sh
===============
- Auto Install Shadowsocks(Go) Server for CentOS/Debian/Ubuntu
- https://teddysun.com/392.html

安装：
```
wget --no-check-certificate -O shadowsocks-go.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-go.sh
chmod +x shadowsocks-go.sh
./shadowsocks-go.sh 2>&1 | tee shadowsocks-go.log
```

卸载：
```
./shadowsocks-go.sh uninstall
```
shadowsocks-crond.sh
===============
- Check Shadowsocks(All version) Server is running or not, and start it if not running
- https://teddysun.com/525.html

安装：
```
wget --no-check-certificate -O /opt/shadowsocks-crond.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-crond.sh
chmod 755 /opt/shadowsocks-crond.sh
```

卸载：
```

```

shadowsocksR.sh
===============
- Auto Install ShadowsocksR Server for CentOS/Debian/Ubuntu
- https://shadowsocks.be/9.html

安装：
```

```

卸载：
```

```

shadowsocks-all.sh
==================
- Auto Install Shadowsocks Server (all version) for CentOS/Debian/Ubuntu
- https://teddysun.com/486.html

安装：
```
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```

卸载：
若已安装多个版本，则卸载时也需多次运行（每次卸载一种）
```
./shadowsocks-all.sh uninstall
```
启动脚本
启动脚本后面的参数含义，从左至右依次为：启动，停止，重启，查看状态。

Shadowsocks-Python 版：
`/etc/init.d/shadowsocks-python start | stop | restart | status`

ShadowsocksR 版：
`/etc/init.d/shadowsocks-r start | stop | restart | status`

Shadowsocks-Go 版：
`/etc/init.d/shadowsocks-go start | stop | restart | status`

Shadowsocks-libev 版：
`/etc/init.d/shadowsocks-libev start | stop | restart | status`

各版本默认配置文件
Shadowsocks-Python 版：
`/etc/shadowsocks-python/config.json`

ShadowsocksR 版：
`/etc/shadowsocks-r/config.json`

Shadowsocks-Go 版：
`/etc/shadowsocks-go/config.json`

Shadowsocks-libev 版：
`/etc/shadowsocks-libev/config.json`

haproxy.sh
===============
- Auto Install haproxy for Shadowsocks Server
- https://shadowsocks.be/10.html

安装：
```

```

卸载：
```

```

Copyright (C) 2014-2019 Teddysun


------------------------------
Update 2019.05.15

使用方法：
使用root用户登录，运行以下命令：

```
wget --no-check-certificate -O shadowsocks-go.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-go.sh
chmod +x shadowsocks-go.sh
./shadowsocks-go.sh 2>&1 | tee shadowsocks-go.log
```

安装完成后，脚本提示如下：

```
Congratulations, Shadowsocks-go server install completed!
Your Server IP        :your_server_ip
Your Server Port      :your_server_port
Your Password         :your_password
Your Encryption Method:your_encryption_method

Welcome to visit:https://teddysun.com/392.html
Enjoy it!
```
卸载方法：
使用 root 用户登录，运行以下命令：

```
./shadowsocks-go.sh uninstall
```

其他事项：
客户端配置的参考链接：https://teddysun.com/339.html

安装完成后即已后台启动 Shadowsocks-go ，运行：

```
/etc/init.d/shadowsocks status
```

可以查看 Shadowsocks-go 进程是否已经启动。
本脚本安装完成后，已将 shadowsocks-go 加入开机自启动。

使用命令：
启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
状态：/etc/init.d/shadowsocks status

多用户多端口配置文件示例：
配置文件路径：/etc/shadowsocks/config.json

```
{
    "port_password":{
         "8989":"password0",
         "9001":"password1",
         "9002":"password2",
         "9003":"password3",
         "9004":"password4"
    },
    "method":"your_encryption_method",
    "timeout":600
}
```
