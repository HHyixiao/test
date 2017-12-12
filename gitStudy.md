创建SSH Key：

```shell
$ ssh-keygen -t rsa -C "youremail@example.com"
```
创建有关电脑的的密钥
```shell
$ ssh-keygen -t rsa
```

git 记住账号密码
```shell
git config --global credential.helper store
```

要关联一个远程库，使用命令`git remote add origin git@server-name:path/repo-name.git`；

关联后，使用命令`git push -u origin master`第一次推送master分支的所有内容，-u 关联分支；



从远程clone `git clone git@github.com:HHyixiao/test.git`

查看远程`git remote -v`

# 分支

创建`dev`分支，然后切换到`dev`分支：`git checkout -b dev`

​	`git checkout` 加 `-b`参数表示创建并切换 == `git branch dev  (创建)  和 git checkout dev (切换)`

查看当前分支：` git branch`

合并指定分支到当前分支:  `git merge dev`(在master分支上执行可以将dev分支合并到主分支)

​	合并时，加上`--no-ff`参数就可以用普通模式合并,例`git merge --no-ff -m "merge with no-ff" dev`

删除分支：`git branch -d dev`  删除dev分支

​	如果要丢弃一个没有被合并过的分支，可以通过`git branch -D <name>`强行删除。

删除远程分支：`git push origin --delete develop` 或者 `git push origin  :develop`

```shell
git fetch origin temp:temp  //拉取远程库temp分支的代码到本地的temp分支，如果不存在temp分支，将自动创建temp分支
```

# 解决冲突

查看分支合并情况`git log --graph --pretty=oneline --abbrev-commit`   `git log --graph`

查看版本记录  `git log --pretty=oneline`

# Bug分支

把当前工作现场“储藏”起来: `git stash`

查看"储藏区": `git stash list`

从"储藏区"恢复到工作区: `git stash apply`  但是恢复后,stash内容并不删除,需要用`git stash drop`来删除;

恢复的同时把stash内容也删除: `git stash pop`

查看"储藏区": `git stash list`  恢复指定的 `git stash apply stash@{0}`


# git版本控制：如何处理当前分支为*（no branch）的情况

git checkout -b 分支名；此时新创建的分支与*（no branch）软件一样，然后切换到主分支，合并





