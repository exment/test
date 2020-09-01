# 操作

## cd 路径 进入目录

## github账号

```sh
# 添加账户名称
git config --global user.name "exment"
# 添加账户名字 邮箱
git config --global user.email "exment@qq.com"
# 没有消息就是好消息 提示信息就说明出错
```

## 概念

1. 工作区 本地磁盘路径
2. 暂存区 虚拟仓库
3. 远程仓库 github

11楼    -》 电梯口（暂存区） -》1楼 
工作区   -》 暂存区         -》远程仓库

## 步骤
1. github 建立远程仓库
2. 本地文件夹 git init 初始化完成之后 目录下有.git文件夹 内存里面的虚拟仓库建立好了
    .git 文件夹 存储当前项目的所有版本信息
    本地的暂存区就好了
```sh
# 建立暂存区
git init
```
3. 本地文件夹 README.md 说明书
    编写程序
4. 工作区 -》 暂存区
```sh
# 工作区 提交暂存区
git add
```
    git add