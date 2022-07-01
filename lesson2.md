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
1. 查看主机名
    * `hostname` - 系统显示本机的主机名。在我的机器上，显示的是ML0-CACHE-HIT。
    * 主机名有点像域名，可以在局域网（同一网段）中替代IP地址。使用主机名，就不怕主机的IP地址变化了。
        * `ping ML0-CACHE-HIT`
        * `ssh ML0-CACHE-HIT`
        * `curl http://ML0-CACHE-HIT/`
1. 拷贝远程文件
    * `scp {source} {dest}`
        * Linux/Win都可用。
        * 支持本地到远程、远程到本地、远程到远程的拷贝。
        * 远程文件的格式为 - `{user_name}@{hostname_or_ip}:{path}`。
        * 文件名可以带通配符。
        * 示例
            * `scp ./cert/*.pem root@ML0-CACHE-HIT:/etc/nginx/cert/`
1. ssh运行耗时脚本
    * 在ssh中运行耗时脚本，一旦ssh终端，运行中的脚本将不复存在。
    * 使用`tmux`可以解决ssh运行耗时脚本的问题。
        * `tmux new -s session_name` - 创建tmux session
        * `watch -n 2 free` - 运行耗时脚本
        * `ctrl + b, d` - detach tmux
        * `tmux ls` - 列举tmux session
        * `tmux a -t session_name` - 恢复tmux session
1. 查看帮助
    * `man netstat`

[上一课](lesson1.md) | [目录](README.md) | [下一课](lesson3.md)
