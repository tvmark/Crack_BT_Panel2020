 
宝塔面板5.9.X Pro破解版一键脚本已完成，欢迎使用。

网上主流的破解方法是导入其他已授权用户的配置信息，部分下载源并非来自宝塔官方渠道，安全性无法保障，本方法全部基于修改本地配置文件实现，安全绿色无后门。

本破解方法的原理是通过劫持宝塔面板的 common.py 里，第 164 行记录 release 的信息，将其延期到 2999 年，实现了永久破解的目的。

使用须知
本脚本必须在完全干净的 CentOS/Debian/Ubuntu 系统上安装

如已安装更高版本的宝塔面板，请先卸载高版本再安装

如已安装其他种类的面板，或 LNMP 之类的运行环境、一键包，建议备份好数据，重装干净系统再安装

使用方法
wget --no-check-certificate -qO crack_bt_panel_pro.sh https://git.io/JvkjT && bash crack_bt_panel_pro.sh

卸载
wget --no-check-certificate -qO uninstall.sh https://git.io/JvkjI && bash uninstall.sh

安装wget
yum -y install wget

更新日志
Nginx 安装器 openssl 主线版本已升级至 1.1.1d 和 1.0.2t；
提供卸载功能；
重新恢复官方安装源，将本仓库作为备份源；
为防止宝塔面板官方封杀此破解方法，面板主安装文件已迁移至本项目仓库，如对安装文件是否有后门等产生疑问，请自行与官方安装文件对比；
默认预置 Nginx 安装器，Nginx 主线版本已升级至 1.15.12，openssl 主线版本已升级至 1.1.1c 和 1.0.2s；
默认开启 ssl 登陆，因 ssl 证书是面板自签的，所以不会被浏览器信任，忽略即可；
由于破解的过程会输出一些命令，导致会把包含初始化登陆信息的输出结果顶到上面去，请在终端里调整滚动条，找到 Bt-Panel：https://你的域名:8888 一项，下面的 username 和 password 即分别是面板安装完成后，默认的用户名和密码。
