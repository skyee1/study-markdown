# github与gitlab远程分支区别
github远程主分支叫main，gitlab远程主分支叫master

# 关联远程仓库

```
# 在本地工作目录下初始化git
git init
# 关联远程仓库
git remote add origin git@git.yasdb.com:zouyi/git_learn.git
```

# 第一次提交

```
# 添加改动文件到暂存区
git add .
# 将暂存区文件提交到本地仓库
git commit -m "first commit"
# 将本地仓库推送到gitlab远程仓库
git push origin master
# 将本地仓库推送到github远程仓库
git push origin main
```

# 分支管理

```
# 获取远程仓库信息
git fetch
# 查看远程仓库信息
git branch -r
# 关联远程分支test
git branch --set-upstream-to=origin/test master
显示Branch 'master' set up to track remote branch 'test' from 'origin'.即为成功
# 查看当前当前分支与远程分支的关联情况
git branch -vv
# 现在可以向远程分支提交改动了
git push origin master:test
使用正确的推送语法：如果你想要推送到远程仓库的一个特定分支，而不是将本地分支与远程分支关联起来，
你可以使用 git push origin <local-branch-name>:<remote-branch-name> 的语法。
将 <local-branch-name> 替换为你的本地分支名称，<remote-branch-name> 替换为你想要推送到的远程分支名称
```

# gitlab或github下fork后如何同步源的新更新内容
https://blog.csdn.net/weixin_43517190/article/details/125159723

设置（更改）远程上游仓库
```
git remote set-url upstream <新的远程仓库URL>
# 例如
git remote set-url upstream https://git.yasdb.com/cod-x/anchor_regress.git
```
同步上游仓库
```
# 查看状态确认是否配置成功
git remote -v
# 同步fork
git fetch upstream
# 切换到本地主分支
git checkout master
# 把 upstream/master 分支合并到本地 master 上
git merge upstream/master
# 推送到远程主分支
git push origin master
```
