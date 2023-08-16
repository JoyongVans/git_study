# git的基础操作

---

## 两种初始化的方式

- git clone 加别人的git链接
    
- git init
    

## 提交操作步骤

- 第一种情况
    

1. git add . 把文件加入暂存区（为准备提交整个工作区的文件）
    
    2. git commit -m "此次提交的备注"
        

- 第二种情况（单独提交一个文件）

-	1. git add 文件名
	2. git commit -m "此次提交的备注"
-  或者 git commit -am “备注” 


## 恢复

git checkout HEAD 加文件名 作用：从最后一次提交里把把文件复制到工作区


## 查看

- git log 
	查看提交的历史记录 （commit 后的长串字符 “哈希值 ”用来唯一标识每次提交）
	git log --all （所有分支）
	git log --all --graph 
- git log --pretty=oneline 简化
![[log查看.png]]

查看所处分支
	- git status
	- git branch --list
		- * 号在哪就所处哪个分支

![[分支 graph查看.png]]
## 创建分支
git branch 加名字(feature1)

## 切换分支
git checkout feature1

新建并切换：git checkout -b feature2
## 修改分支上的代码
vi 文件名
	- i 进入插入模式
	（修改）
	- esc键
	- :wq （退出）

![[分支修改 并查看.png]]
## 合并分支
git merge  feature1
![[合并分支1.png]]
### 出现冲突
![[出现冲突.png]]
最终合并
	把等号上方或者下方的删除，保留想要的。
![[最终合并.png]]

### 创建远程仓库

git remote add 名字 链接 

### 把本地代码推送到远程仓库里

git push 远程仓库(此处为origin） 分支