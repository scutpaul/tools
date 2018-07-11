今天使用apt-get update 出现
E: 无法获得锁 /var/lib/apt/lists/lock - open (11: 资源暂时不可用)
E: 无法对目录 /var/lib/apt/lists/ 加锁
第一次发现，不明原因。问度娘

在网上搜索到的解决方案──“将/var/lib/apt/list/lock删除掉即可”──其实是一种极端的情况，也就是在上次更新没有正常关闭的情况下使用。
在大部分情况下，问题的原因在于其它的程序如系统的自动更新、新立得等正在使用apt-get进程，所以解决方法也就是将这一进程关闭。
具体如下：
1、ps-aux 查出apt-get进程的PID，通常是一个四位数字。
2、用kill PID代码 杀死进程
3、用apt-get update，sudo apt-get dist-upgrade升级。

方法一：
执行一下 sudo dpkg --configure -a
方法二：
sudo rm /var/lib/apt/lists/lock
方法三：
1、ps-aux 查出apt-get进程的PID,
2、用sudo kill PID代码 杀死进程(我都是找出带apt字样的进程格杀勿论)

我用的方法一