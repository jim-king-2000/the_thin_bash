# 4. bash脚本

## bash脚本启动
1. 新建一个shell（子进程），然后在新shell中运行脚本。脚本中修改/新增的环境变量，在脚本运行结束后，随着新shell一起消失。
    * `bash my_script.sh`
    * `./my_script.sh` (使用这种方式，my_script.sh必须拥有运行权限)

1. 在当前shell运行脚本。脚本中修改/新增的环境变量，在脚本运行结束后继续有效。
    * `source my_script.sh`
    * `. my_script.sh`

1. bash脚本调试。将脚本中每一条命令和结果都打印出来。
    * `bash -x my_script.sh`


[上一课](lesson2.md) | [目录](README.md) | [下一课](lesson4.md)
