创建SSH Key：

```shell
$ ssh-keygen -t rsa -C "youremail@example.com"
```



要关联一个远程库，使用命令`git remote add origin git@server-name:path/repo-name.git`；

关联后，使用命令`git push -u origin master`第一次推送master分支的所有内容，-u 关联分支；



从远程clone ` git clone git@github.com:HHyixiao/test.git`

# 分支

创建`dev`分支，然后切换到`dev`分支：`git checkout -b dev`

​	`git checkout` 加 `-b`参数表示创建并切换 == `git branch dev  (创建)  和 git checkout dev (切换)`

查看当前分支：` git branch`

合并指定分支到当前分支:  `git merge dev`(在master分支上执行可以将dev分支合并到主分支)

删除分支：`git branch -d dev`  删除dev分支