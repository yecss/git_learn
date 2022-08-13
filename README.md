# 这可能是最简洁的 Git 教程

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

```
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

```
git diff
```

## git commit

## git remote

连接远程仓库，假如我们不是从远程 clone 了一个仓库到本地，而是直接从本地新建了一个仓库的话，那我们想要将代码推送到远程仓库，我们就需要连接到远程仓库。

```
git remote add origin <server>

# origin 是一个别名叫什么都可以，add 相当于给这个远程仓库添加一个叫origin的别名，方便后续的push
```

##
