# 环境变量

## 设置环境变量
1. 设置环境变量，仅在当前进程有效。我们称之为非导出的环境变量。
    * `name=value`
1. 设置环境变量，使其可以被子进程继承。我们称之为导出的环境变量。
    * `export name` - 这里的`name`，是之前使用`name=value`命令设置过的非导出环境变量的名称。
    * `export name=value` - 新建一个导出的环境变量。

# 设置`PATH`环境变量
1. `export PATH=path0:path1:path2`
2. 示例
    * `export PATH=/home/jim/.local/bin`
    * `export PATH=/home/jim/.local/bin:/usr/local/sbin`
    * `export PATH=$PATH:/home/jim/.local/bin:/usr/local/sbin`
