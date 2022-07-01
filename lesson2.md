# bash常用命令

## 查看系统情况
1. 查看版本
    * `lsb_release -a` - 查看Linux发行版版本。
    * `uname -a` - 查看Linux内核版本。
1. 查看资源占用
    * `htop`
1. 查看磁盘占用
    * `df -hl`
1. 查看文件和目录大小
    * `du -h --max-depth=1`

## 查看网络
1. 查看所有网卡的信息
    * `ifconfig`
1. 查看域名解析
    * `dig www.baidu.com`
    * `nslookup www.baidu.com`
1. 查看端口占用
    * `lsof -i:22`
    * `netstat -anp`
    * `ss -anp`
1. 查看本机IP地址
    * `hostname -I`
