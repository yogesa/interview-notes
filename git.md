# Git

git 是一个分布式的版本控制工具.

### 如何让自己的主机在分布式网络中确认身份?

```git config```   ```--global ```这台机器上的所有仓库都会使用这个配置

通过 ```git config```   ```--global ``` 配置主机

```shell
$git config --global user.name "chenhui"
$git config --global user.email "1316238389@qq.com"
```

### 使用Git

1 在想要要建立仓库的目录下, 初始化仓库

```shell
$ git init
```

2 将仓库下的文件添加到暂存区

```shell
$ git add a.txt 
// 也可以将仓库下的所有文件放入仓库 
$ git add *
```

3 用 ```git commit``` 告诉 Git , 把暂存区提交到仓库

```shell
$ git commit -m "write a readme file"
```

<font color="red">Q1 : 为什么 ```add``` 和```git commit``` 弄这么麻烦, 先要添加, 再要提交, 弄两次添加文件 ? </font>

​	因为 add 可以一次添加一个文件, 而提交可以多次添加将添加的文件一同进行提交.

4 掌握仓库的实时状态

```shell
git status
```

5 查看仓库中与本地不同的文件，并且查看本地修改了哪里

```shell
git diff
```

6 版本回退

HEAD 指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令  `git reset --hard commit_id`

- 穿梭前，用`git log`可以查看提交历史，以便确定要回退到哪个版本。
- 要重返未来，用`git reflog`查看命令历史，以便确定要回到未来的哪个版本。

7 管理与修改

当新建了一个文件 b.txt,  git add b.txt 添加至缓存区，git commit -m "" 会将缓存区的内容添加至仓库

当新建了一个文件b.txt, git add b.txt 添加至缓存区，修改 b.txt 后，git commit -m “”  会将第一次添加的 b.txt 添加至仓库

查看仓库与本地的文件不同：

```shell
git diff HEAD -- readme.txt
```

