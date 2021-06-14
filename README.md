# Day01
Git和GitHub入门

### 作业

1、场景一：把现有的项目或新项目用Git管理；场景二：从远程仓库克隆到本地（推荐）至少操作3遍！

2、预习 Git 技巧篇。

### 主要内容

### 一、如何安全高效地管理代码？

1、场景一：把现有的项目或新项目用 Git 管理

```
$ mkdir test 

$ cd test

$ git init

$ touch readme.txt

$ git add readme.txt

$ git commit -m "add readme.txt"

简单解释一下 git commit 命令，-m 后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录。

$ git status

$ git remote add origin 远程仓库URL

执行推送或者拉取的时候，如果省略了远程仓库的名称，则默认使用名为 ”origin“ 的远程仓库。因此一般都会把远程仓库命名为 origin 。

$ git push origin master

PS：当被要求输入用户名和密码，请使用你在GitHub的用户名和密码。

由于远程仓库是空的，我们第一次推送 master 分支时，加上了-u参数，Git 不但会把本地的 master 分支内容推送到远程新的 master 分支，还会把本地的 master 分支和远程的 master 分支关联起来，那么下一次推送时就可以省略分支名称了。但是，首次必须指定远程仓库名称和分支名称。

```

2、场景二：从远程仓库克隆到本地（推荐）

```
$ git clone 远程仓库URL

PS：当被要求输入用户名和密码，请使用你在 GitHub 的用户名和密码。

$ cd 远程仓库目录名

$ touch README.md

$ git add README.md

$ git commit -m "add Readme.md"

$ git push
```


### 二、如何快速高效地获取他人优秀代码？

GitHub官网：https://github.com/


### 三、Git 技巧篇

#### 1、给文件重命名的简便方法

```
$ git clone 远程仓库地址

$ cd 远程仓库目录

$ touch README.txt

$ git add README.txt

$ git commit -m "add readme.txt"

$ git push

$ git log

常规做法

$ mv README.txt README.md

$ git status

$ git add README.md

$ git rm README.txt

$ git status

$ git commit -m "rename readme"

$ git log

彻底回退到某个版本

$ git reset --hard 版本号（必须慎用！！！）

$ git log 

简便做法：

$ git mv README.txt README.md

$ git status

$ git commit -m "rename readme"

$ git log

```

#### 2、正确删除文件的方法

```
常规做法：

$ rm readme.md

$ git rm readme.md

简便做法：

$ git rm readme.md

```
