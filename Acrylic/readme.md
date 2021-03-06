卡饭地址: http://bbs.kafan.cn/thread-2039048-1-1.html<br/>
github地址: https://github.com/miaomiaosoft/Acrylic-DNS-Proxy-GUI

这个软件的意义在于使用更好的缓存加速本机DNS二次解析速度+防DNS污染+强大的本地HOSTS功能+有效防止在线DNS不稳定导致的网站打不开等问题！

####简单教程：
1. 以管理员权限运行，点击“启动服务”，弹出成功提示即为启动成功。

2. 然后点击“设置DNS”会帮你设置好默认名为本地连接的DNS地址。

3. 最好到宽带连接属性里查看DNS是否设置正确，如不正确请自行设置一下DNS：
    IPV4为  127.0.0.1
    IPV6为  ::1

####想折腾的：
1. 可以修改下配置，UDP协议会比TCP协议解析更快，不过TCP协议通常可以防止DNS污染，所以如果自己所在地区的DNS污染较严重可以尝试改成使用TCP解析（配合HTTPS，你应该懂的！）【07.06更新：测试发现TCP解析有时会被墙阻断，不推荐使用】。

2. 有些地区运营商自带墙中墙，会强制劫持DNS使用的53端口，此时可以在配置里更改使用其他端口来绕过劫持，通常多数DNS都支持53和5353（自建DNS服务器也可以使用其他端口，自行指定）。

3. 自定HOSTS功能相比系统自带的HOSTS强N倍，支持二级域名通配符“*”和泛解析通配符“>”，支持单一条目同一IP匹配多个域名，支持在正则域名内排除域名，支持正则表达式等等，反正想折腾你可以看配置说明和示例研究一下。

4. 在配置里可以使用“^*”来排除解析某个域名，排除后会转用其他备用DNS解析，通俗讲就是你可以配置不同的DNS解析不同的域名，也可以配置某个DNS只解析某几个特定域名，还可以配置只解析A记录或AAAA记录类型，具体参照配置说明和示例。

####注意事项：
1. 软件以服务方式运行，只要启动服务成功，即为开机自启！

2. 软件带设置系统DNS功能，需管理员权限，可能被某些国内杀软件误报病毒，反正我的ESET不报，请自己鉴别！（好吧，其实就是请360用户别用！）

3. 如不能在GUI上启动服务，请到软件目录下管理员权限运行“InstallAcrylicService.bat”启动！

4. 如果需要升级程序，请先备份HOST和配置文件，再停止服务（如有错误提示为正常），最后复制新版文件替换后再启动服务！

5. 默认内置IPV6的DNS，有些用户宽带支持IPV6解析但不能与IPV6通信导致网站打不开的情况下，请自行把IPV6DNS的所有参数清空！

6. 和系统DNS一样，解析数据也是有缓存的，有时网站更新了IP地址然而本机还是旧IP可能导致网站打不开，这时你需要手动在程序上清空缓存解决！