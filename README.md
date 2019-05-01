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
