
# Shell 学习笔记 常用命令

## Linux 命令三剑客
* grep 查找
* sed 替换
* awk 是一种处理文本文件的语言，是一个强大的文本分析工具

## 获取路径的目录名 dirname

```shell
echo $(dirname "${目录路径}")
```

## 获取上一条命令的返回结果

* 一种是`$?`
* 一种是`PIPESTATUS[]`数组，对应每一条命令的执行结果，比如用PIPESTATUS[0]获取第一个或者所有的PIPESTATUS[@]

## 目录切换命令 cd pushd popd dirs
- 一般我们用的都是`cd`，只有通过命令切换目录，那么`dirs`命令就能显示目录栈，比如`dirs -v` 或者`dirs -p`，清楚目录栈`dirs -c`
- `pushd` 和`popd`是成对使用的，使用`pushd` + or - 目录索引，可以方便进入到某个目录

## 获取文件大小
```shell
以方便阅读的方式打印当前 目录层级为1的文件大小

du -h -d 1
```

## 计数命令

```shell
 wc 命令用于计算字数
```

## 获取系统类型
```shell
echo $OSTYPE
```