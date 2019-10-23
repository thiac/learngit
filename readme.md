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
- git checkout -- file: 撤销修改 
- git rm file: 版本库中删除文件

## git 远程仓库
- git remote add origin git@github.com:thiac/learngit.git: 关联仓库
- git push -u origin master: 推送master所有内容
- git checkout -b bran: 创建分支并转换到该分支
- git branch: 列出所有分支，带*表示当前分支
- git merge bran: 合并分支
- git branch -d bran: 删除分支
- git merge --no-ff -m "merge with no-ff" dev: 加上no-off参数就可以用普通模式合并，能看出曾经做过合并
- git stash: 保存当前工作现场 

