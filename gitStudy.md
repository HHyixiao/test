创建SSH Key：

```shell
$ ssh-keygen -t rsa -C "youremail@example.com"
```



要关联一个远程库，使用命令`git remote add origin git@server-name:path/repo-name.git`；

关联后，使用命令`git push -u origin master`第一次推送master分支的所有内容；