创建SSH Key：

```shell
$ ssh-keygen -t rsa -C "youremail@example.com"
```



要关联一个远程库，使用命令`git remote add origin git@server-name:path/repo-name.git`；

关联后，使用命令`git push -u origin master`第一次推送master分支的所有内容；



从远程clone ` git clone git@github.com:HHyixiao/test.git`

# 分支

创建`dev`分支，然后切换到`dev`分支：`git checkout -b dev`

​	`git checkout`命令加上`-b`参数表示创建并切换 == `git branch dev	和	git checkout dev`