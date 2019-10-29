# git 命令学习

## git 本地操作
- git init: 初始化本地仓库 
- git add file: 将修改添加到暂存区
- git commit -m " 提交到分支
- git status: 查看状态
- git log: 历史记录
- git reset --hard HEAD^: 回退到上一个版本
- git reflog: 记录每一次cmd
- git diff HEAD -- file: 命令可以查看工作区和版本库里面最新版本的区别
- git diff --cached/stage
- git checkout -- file: 撤销修改 
- git rm file: 版本库中删除文件

## git 远程仓库
- git remote add origin git@github.com:thiac/learngit.git: 关联仓库
- git push -u origin master: 推送master所有内容
- git pull: 拉取远程内容
- git checkout -b bran: 创建分支并转换到该分支
- git branch: 列出所有分支，带*表示当前分支
- git merge bran: 合并分支
- git branch -d(D) bran: (强制)删除分支
- git merge --no-ff -m "merge with no-ff" dev: 加上no-off参数就可以用普通模式合并，能看出曾经做过合并
  ff(Fast foward)
- git stash: 保存当前工作现场 
- git stash list: 列出工作现场列表 
- git stash apply: 恢复
- git stash drop: 删除
- git stash pop: 边恢复边删除（以上两步动作的结合）
- git log --graph --pretty=oneline --abbrev-commit 产看分支合并图
- git rebase: 本地未push的分叉提交历史整理成直线，使查看历史提交更方便
- git tag v××: 创建标签
- git tag v×× commitID: 标签关联
- git tag: 展示所有标签
- git show tag: 展示标签内容
- git tag -a 标签名 -m "commit" cimmitID
- git tag -d v××: 删除标签
- git push origin tag/--tags: 可以推送一个本地标签/全部未推送标签
- git push origin :refs/tags/tagname: 可以删除一个远程标签
- git config --list: 列出所有已配置的选项
