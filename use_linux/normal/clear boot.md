//查看boot中的文件
dpkg --get-selections |grep linux-image

//当前使用的版本
uname -a

//清理
sudo apt-get autoremove linux-image-4.4.0-31-generic linux-image-4.4.0-34-generic

//删除配置
sudo dpkg -P linux-image-4.4.0-31-generic