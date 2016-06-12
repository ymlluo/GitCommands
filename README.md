# GitCommands

git 常用命令汇总

git config user.name #配置用户名

git config user.email #配置邮箱

git config credential.helper store #保存远程用户名密码 --cache 保存在内存中

git init #初始化版本库 --bare #裸库(服务器端，不包含工作区)

git add #添加文件到版本库

git commit -m "info" #提交到版本库

git commit -a -m "info" # 跳过添加文件步骤 提交到版本库

git commit --amend #尝试重新提交

git reset HEAD #来取消暂存,修改为未暂存

git checkout -- #撤消对文件的修改

git status #查看状态

git diff #查看修改（比较），--cahce 和--staged

git log #查看日志 --oneline 单行显示 --graph #查看分支合并图

git reset --hard HEAD^ #恢复到上一个版本 windows下使用2个^（^^)

git reset --hard #恢复到特定版本

git reflog #查看版本记录

git rm #删除文件&从版本库中删除不在跟踪 --cache 仅删除版本库不删除本地文件 可以git checkout -- 恢复删除

git remote add pb #添加远程库

git fetch [remote-name] #从远程仓库中获得数据 默认：git fetch origin

git pull 抓取然后合并远程分支到当前分支

git push [remote-name] [branch-name] #推送到远程仓库 如：git push origin master

git remote -v #查看远程库信息

git remote show origin #查看远程仓库

git remote rename [name] [branch-name] #修改一个远程仓库的简写名

git remote rm [branch-name] 移除一个远程仓库

git branch #查看分支

git branch #创建分支

git checkout #切换到分支

git checkout -b # 创建并切换 到分支

git merge #合并某分支到当前分支 --no-ff 禁用Fast forward（）

git branch -d #删除分支

git branch -D #强制删除没有被合并过的分支

git ls-remote (remote) #获得远程分支的完整列表

git remote show (remote) #获得远程分支的更多信息

git push (remote) (branch) #创建远程分支 如：git push origin serverfix 协同工作时 一人创建，其他人拉取在 追踪即可

git fetch origin #从服务器上抓取数据

git fetch --all #取所有的远程仓库

git pull #拉取并合并

git merge (remote)/(branch) #将远程分支合并到当前所在的分支

git checkout -b [branch] [remotename]/[branch] # 跟踪分支 -到- 其他远程仓库上的跟踪分支

git checkout --track origin/serverfix #上面命令的快捷写法

git branch -u origin/serverfix #设置已有的本地分支跟踪一个刚刚拉取下来的远程分支，或者想要修改正在跟踪的上游分支

git branch -vv #所有的本地分支列出来并且包含更多的信息

git push origin --delete (branch) #从服务器上删除 分支

git stash #保护现场 把未提交的文件保存起来，保持工作区clear

git stash list #查看保护的现场列表

git stash apply #恢复现场 并保留现场文件不删除用git stash drop来删除 git stash apply stash@{0}

git stash pop #恢复现场的同时把stash内容也删除掉

git tag #查看所有标签

git tag -l 'v1.8.5*' #查找标签

git tag -a v1.4 -m 'my version 1.4' #附注标签 存储在 Git 数据库中的一个完整对象

git show v1.4 标签详情

git tag v1.4 ####只会显示出提交信息

git log --pretty=oneline 查看ID

git tag -a v1.2 9fceb02 未指定ID打标签 -s用私钥签名一个标签

git tag -d v0.1 #删除标签

git push origin v1.5 #推送标签到远程服务器

git push origin --tags #推送全部标签

git push origin :refs/tags/v0.9 #删除远程标签

git checkout -b [branchname] [tagname] #在特定的标签上创建一个新分支
