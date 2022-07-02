# 环境变量

## 设置环境变量
1. 设置环境变量，仅在当前进程有效。我们称之为非导出的环境变量。
    * `name=value`
1. 设置环境变量，使其可以被子进程继承。我们称之为导出的环境变量。
    * `export name` - 这里的`name`，是之前使用`name=value`命令设置过的非导出环境变量的名称。
    * `export name=value` - 新建一个导出的环境变量。

## 设置`PATH`环境变量
1. `export PATH=path0:path1:path2`
1. 示例
    * `export PATH=/home/jim/.local/bin`
    * `export PATH=/home/jim/.local/bin:/usr/local/sbin`
    * `export PATH=$PATH:/home/jim/.local/bin:/usr/local/sbin`

## 显示某个环境变量的值
1. `echo $name` - 同时支持导出的和非导出的环境变量。
1. `printenv name` - 只支持导出的环境变量。

## 列举当前所有的环境变量（只支持列举导出的环境变量）
1. `env`
1. `printenv`
1. `export`

## 删除环境变量（支持导出的和非导出的环境变量）
1. `unset name`

## 永久设置环境变量
1. 将`export name=value`语句写到环境变量定义文件中去。
    * 用户级别环境变量定义文件
        * ~/.bashrc
        * ~/.profile
        * ~/.bash_profile
    * 系统级别环境变量定义文件
        * /etc/bashrc
        * /etc/profile
        * /etc/bash_profile
        * /etc/environment

## 为某一个进程设置专属环境变量
1. `name0=value0 name1=value1 command`
2. 示例
    * `NODE_OPTIONS=--openssl-legacy-provider DEBUG=oidc-provider:* ISSUER=http://localhost:7000 MONGODB_URI=mongodb://test:111@47.97.195.81:8282/test nodemon src/server.mjs --watch src`


[上一课](lesson3.md) | [目录](README.md) | [附录](appendix.md)
