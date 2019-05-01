# git-study


# 场景：主线开发时，需要临时添加一个功能或修复一个bug，则新建一个分支
	git branch branchName	# 新建 branchName 分支
	git checkout branchName	# 切换到 branchName 分支
	或者
	git checkout -b branchName # 创建 branchName 分支并切换到改分支
	
	... 进行 bug 修复 ...
	
	git status # 查看变动
	
	git add . # 让 git 追踪所有变动文件
	git commit -m “变动说明” # 提交到本地仓库
	或者
	git commit -a -m "变动说明" # 追踪所有变动文件并提交到本地仓库
	
	
	git push origin branchName # 将修改后的变动推送到远程并在远程建立 branchName 分支
	
	
	git checkout master # 切换到 master 切换到 master 分支
	
	git merge branchName # 将修改合并到 master 分支
	
	git branch -d branchName # 删除本地分支
	
	git push origin :branchName # 删除远程分支
	
	
# 场景：1，只对文件进行了修改，未执行任何 git 操作；2，执行了 add 操作后回退；3，执行了 commit 操作后回退；4，执行了 push 操作后回退

	git checkout -- changedFileName # 场景1，只进行了修改操作。丢弃修改的操作
	
	
	git reset HEAD .	# 场景2，执行 git add后。丢弃追踪的文件
	git checkout -- . # 丢弃修改的操作
	
	
	git reflog # 场景3，执行 commit 操作之后。查看版本变动记录
	
	git reset --hard head^ # 回退一个版本
	或者
	git reset --hard  HEAD@{5} # 回退到指定版本
	
	