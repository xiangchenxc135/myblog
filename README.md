# Git
Git（读音为/gɪt/）是一个开源的分布式版本控制系统，可以有效、高速地处理从很小到非常大的项目版本管理。 [1]  也是Linus Torvalds为了帮助管理Linux内核开发而开发的一个开放源码的版本控制软件。

Git的作用是用于管理项目的源代码 
它主要用于管理 开发环境(Dev)下的项目代码

市面上主要有两类源代码管理工具
1. 集中式代码管理工具 (svn)
2. 分布式代码管理工具 (git)

官网
https://git-scm.com/
git 是一个跨平台的项目管理工具 可以运行在 Windows Linux Unix OSX

### git基本操作
#### 全局用户配置
```bash
# 每台计算机只需要执行一次配置
$ git config --global user.name 'Zhang Jun'
$ git config --global user.email 'root@rootbk.cn'
```

1. 项目构建 在项目的根目录创建文件 (README.md      .gitignore)
2. 在 .gitignore 中 存放需要忽略的文件或目录 (不需要git管理的文件或目录)
3. 在项目的根目录 执行 `$ git init` 进行仓库初始化操作
4. 进行项目初始化 `$ npm init -y`


#### 本地仓库操作
```bash
# 查看状态
$ git status

# 添加管理(将文件或目录添加到git本地仓库的暂存区)
$ git add filename    # 添加文件到暂存区
$ git add .           # 添加当前目录所有内容到暂存区
$ git add path/       # 添加指定目录到暂存区
$ git add --all       # 添加所有内容到暂存区

# 将文件移出暂存区
$ git rm --cached filename

# 将暂存区的内容提交到本地仓库
$ git commit -m 'message'

# 查看提交日志
$ git log

# 恢复版本
$ git reset --hard 提交记录的前6位

# 查看帮助
$ git --help

# 恢复文件
$ git checkout filename
```


#### 远程仓库操作
```bash
# 设置远程仓库地址
$ git remote add origin https://github.com/jxsrzj0325/suning.com.git

# 将本地仓库提交到远程仓库
$ git push -u origin master

# 查看所有源
$ git remote

# 查看源的路径
$ git remote get-url 名称

# 克隆仓库(下载 从无到有)
$ git clone https://gitee.com/rootbk/suning.com.git

# 拉取(已有 更新)
$ git pull origin master
```
