## 通过命令添加多个仓库

### 1.查看现有几个仓库


git remote -v

2.添加一个远程仓库
添加一个远程库 名字不能是origin

git remote add testAdd  http://git.test.com/tsest/test.git   
1
3.推送拉取代码
拉取代码

git pull testAdd    远程分支名：本地分支名
1
推送代码

git push testAdd    远程分支名：本地分支名

二、修改git配置文件添加多个仓库
1.在你本地仓库的config文件夹里面找到.git文件，然后修改
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
	ignorecase = true
	precomposeunicode = true
[remote "origin"]
	url = 第一个远程仓库url
	url = 第二个远程仓库url
	url = 。。。
	以此类推
[branch "branch1"]
	remote = origin
	merge = refs/heads/branch1
[branch "branch2"]
	remote = origin
	merge = refs/heads/branch2
 

2.推送拉取代码
与推送拉取一个仓库没有区别，直接操作就好了

git pull    会自动拉取代码

git push    会自动推送代码到两个远程仓库

