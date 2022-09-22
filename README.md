# 这可能是最简洁的 Git 教程
[TOC]
## 前言

git 是一个分布式的项目管理工具，和其他的管理工具不同。他是分布式的。

他有三个状态：

-   Modified - 已修改

-   Staged - 已暂存

-   Commited - 已提交

## 安装 Git

1、下载 Git, 可以使用镜像网站下载：https://registry.npmmirror.com/binary.html?path=git-for-windows

2、在安装的过程中，一般都是使用默认配置，不需要去修改。(要注意的配置项可能是配置默认编辑器和 terminal)

3、安装完成之后，打开 git 配置一些基本的用户信息,如邮箱，用户名。

```bash
git config --global user.name "John Smith"

git config --global user.email john@example.com
```

## git add

将我们修改过的文件添加到暂存区，暂存区的意思是一个临时的区域，在我们将代码提交到仓库前，需要经过的一个区域。

这就好比我们去寄快递需要经过快递驿站，然后将快递送达到目的地。

```bash
git add .
# 将当前文件夹所有的文件添加到暂存区

git add <filename>
# 添加指定的文件到暂存区

# demo
# git add README.md
```

## git status

查看当前文件的状态，可以看出哪些文件修改了，哪些文件处于暂存区。方便我们的操作。

```bash
git status

git status -s #简洁的查看
```

## git diff

查看当前修改的文件和原文件的区别

```bash
git diff
```

## git commit

将暂存区的文件真正的提交到仓库中

```
git commit -m "本次提交信息"

# 在开发时，良好的习惯是根据工作进度及时 commit
# 并务必注意附上有意义的 commit message。创建完项目目录后
# 第一次提交的 commit message 一般为「Initial commit.」。
```

## git remote

连接远程仓库，假如我们不是从远程 clone 了一个仓库到本地，而是直接从本地新建了一个仓库的话，那我们想要将代码推送到远程仓库，我们就需要连接到远程仓库。

```bash
git remote add origin <server>

# origin 是一个别名叫什么都可以，add 相当于给这个远程仓库添加一个叫origin的别名，方便后续的push
```

## git clone

将一个远程仓库克隆到本地上

```bash
git clone https://github.com/yecss/git_learn.git

# clone的地址获取：点击 github项目的Code按钮，即可看到了。
```

## git log

查看当前项目 git 操作的历史记录

```bash
git log

git log --graph #以图标形式查看
```

## git branch

有关分支的一些操作

```bash
# 列举当前仓库的分支
git branch

# 新增分支
git branch 分支名

# 删除分支
git branch -D 分支名

```
## 设置代理

```bash
git config --global http.proxy 'socks5://127.0.0.1:1080'
git config --global https.proxy 'socks5://127.0.0.1:1080'
# 将后面的端口号也就是1080修改为自己的代理软件的端口
```

## 清除代理
```bash
git config --global --unset http.proxy
git config --global --unset https.proxy
```
