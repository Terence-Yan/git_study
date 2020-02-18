### *********git 命令*********

#### 1.将远程仓库的文件导入到本地：git clone+远程仓库地址

#### 2.查看用户的注册信息：git config --list

#### 3.查看文件状态：git status

#### 4.使用Git Bash命令时，查看Windows系统当前的编码格式：echo $LANG

#### 5.改变系统的当前编码格式：export LANG=en_US.UTF-8(设置为UTF-8编码格式)或 export LANG=zh_CN.GBK  (设置为中文编码格式)，
执行该命令，改变的将只是当前会话的编码，新建会话或重启系统，都将恢复至初始默认值。

#### 6.给项目添加新文件夹
```
1.下载项目到本地：git clone <project-url>
2.查看项目状态：git status
3.在本地编辑项目，添加新文件夹
4.进入新添加的文件夹所在目录(即父目录)，查看项目状态：git status
5.将要提交的新文件夹加入待提交列表：git add <file-name>
6.提交本次添加操作：git commit -m "提交日志"
7.将本次更新推到github上：git push（需要用户名与密码）
```

#### 7.查看(编辑后的)工作区域与Git仓库的差异：git diff --color

#### 8.提交工作区域所有已修改的文件到暂存区域：git commit -a -m <提交日志> 
```
"-m <提交日志>"这个参数是必须要带的，否则git shell客户端会进入vim模式，要求用户在要提交的所有已编辑的
文件上逐一添加“提交日志”后，方可执行提交操作。
```

#### 9.在本地创建新的项目分支
```
1.克隆一个远程分支：git clone -b <指定的分支名称> <git仓库url>，“-b <指定的分支名称>”参数不带的话，默认
克隆的是master分支。
2.创建本地新的分支：git checkout -b <新建分支名称>
```

#### 10.将本地的新建分支push到git仓库
```
git push --set-upstream <repoName> <branchName>
repoName：要推送到的远程仓库的名称，默认是origin
branchName：新建分支在git仓库中的名称，因为是新建分支，所以在远程仓库还不存在，与本地的新建分支名称可以不同
```

#### 11.将指定分支A合并到目标分支M
```
git checkout <目标分支M> : 切换为目标分支
git pull: 拉取(目标分支M的)最新代码 
git merge <要合并的分支A> -m <合并日志>：合并指定分支A
```






