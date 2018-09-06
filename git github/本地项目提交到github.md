# 本地项目提交到github

[TOC]

## 1.在github上创建一个空的项目

![屏幕快照 2018-09-05 20.28.35](/Users/xingxiaoshuai/Documents/doc/images/屏幕快照 2018-09-05 20.28.35.png)

## 2.按提示将本地项目提交到github上

```
git remote add origin https://github.com/xxsvip/doc.git
git push -u origin master
```

git remote add origin https://github.com/xxsvip/doc.git：

本地设置将要提交到远端的仓库地址，起名叫做origin（叫origin是约定俗成）。如果有多个远端仓库的话可以再新增，但是起个其他名字。

可以使用

```
git remote -v
```

来查看远端仓库的地址

可以使用

```
git push origin master
```

将项目push到origin远端仓库的master分支上。

```
git push -u origin master
```

加上-u参数以后只需要输入 **git push**就会自动提交到origin仓库的master分支了。