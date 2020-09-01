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
git add 文件名
git add * 提交所有文件

git commit -m "这一次提交的描述"
```

5. 工作区状态

```sh
# 当前工作区状态 是否有改变的文件
git status

# 从暂存区将文件恢复到工作区
git checkout index.html

# 查看修改 工作区和暂存区版本区别
git diff

# clear 清空控制台

# 查看已经提交过的历史版本
git log

# 恢复文件到指定的某一个版本
# 退回到上一个版本
git reset --hard HEAD^ 
# 退回两个版本
git reset --hard HEAD^^

git reset --hard 指定版本号
```

6. 远程仓库

不能随意提交
必须让github对自己电脑授权

* ssh密钥
ssh-keygen -t rsa -C "github邮箱账户"
用户家目录的.ssh文件夹下生成
id_rsa.pub

* github 上打开 个人中心settings
SSH 选项 新增一个刚才看到的id_rsa.pub文件

* 暂存区-》远程仓库
```sh
# 本地仓库添加了github上的git仓库作为远程仓库，起名origin
# git remote add 添加远程仓库 origin 远程仓库名字 可以自定义 后面再加上url
git remote add origin https://github.com/exment/test.git
# 查看远程仓库 看到远程仓库已经添加成功 fetch用于拉取push用于推送
git remote -v
# 把本地仓库的变化连接到远程仓库主分支
git pull origin master
# 在pull命令后加上 --allow-unrelated-history 合并两个独立启动仓库的历史
# 将远程昂库文件拉取到本地仓库
git pull origin master --allow-unrelated-histories
# 把本地仓库的文件推送到远程仓库
# git push 远程主机名 本地分支名:远程分支名
git push -u origin master
```

* 使用git clone 就不会出现类似问题

提交过程中 可能输入用户名密码