# 这可能是最简洁的 Git 教程

## 前言

git 是一个分布式的项目管理工具，和其他的管理工具不同。他是分布式的。

他有三个状态：

-   Modified - 已修改

-   Staged - 已暂存

-   Commited - 已提交

## git add

将我们修改过的文件添加到暂存区，暂存区的意思是一个临时的区域，在我们将代码提交到仓库前，需要经过的一个区域。

这就好比我们去寄快递需要经过快递驿站，然后将快递送达到目的地。

```bash
git add .
git add <filename>

# demo
# git add README.md
```
