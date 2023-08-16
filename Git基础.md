# git的基础操作
---
## 两种初始化的方式
- git clone 加别人的git链接
- git init

## 提交操作步骤
- 第一种情况
1. git add . 
	把文件加入暂存区（为准备提交整个工作区的文件）
   2. git commit -m "此次提交的备注"

- 第二种情况（单独提交一个文件）
1. git add 文件名
2. git commit -m "此次提交的备注"


## 恢复
git checkout HEAD 加文件名
	作用：从最后一次提交里把把文件复制到工作区

![[Pasted image 20230816182132.png]]

## 查看
git log 
	查看提交的历史记录
		（commit 后的长串字符 “哈希值 ”用来唯一标识每次提交）

![[Pasted image 20230816182034.png]]

![[Pasted image 20230816182245.png]]

## 远程仓库
### 创建远程仓库
git remote add 名字 链接
![[Pasted image 20230816182452.png]]

### 把本地代码推送到远程仓库里
git push 远程仓库(此处为origin） 分支