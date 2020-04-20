---
date: "2019-05-23"
title: "git是什么"
---
caption="Hello Friend!" captionPosition="right" captionStyle="color: red;" >}}
Git是当前世界上最先进的分布式版本控制系统。

常用命令

git clone git clone代码库的url

将线上库克隆到本地

git添加将工作区的修改提交到暂存区

git提交将暂存区的文件或目录提交到版本库区

git推将提交到本地库中的内容推送到远程库中

让git记住密码的命令：
```
git config --golobal credential.helper store 
```

清掉配置：
```
git config --system --unset ctedential.helper  
```
没有add的时候像回退：
```
git checkout .
```
当你已经添加了，后悔了重置命令：
```
git reset HEAD  git checkout .
```
查看提交日志：
```
git log
```
git commit之后后悔了：
```
git reset --hard git日志号
```