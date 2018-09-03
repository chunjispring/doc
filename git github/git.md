# git

[TOC]

## git是什么

![屏幕快照 2018-09-03 11.24.51](../images/屏幕快照 2018-09-03 11.24.51.png)



![屏幕快照 2018-09-03 11.14.00](../images/屏幕快照 2018-09-03 11.14.00.png)

## git基本命令

```
git config用来区分每次提交的用户
git config --global user.name "xiaoshuai xing"
git config --global user.email "xxs@email.com"
查看当前的用户和对应邮箱：
git config --global user.name
git config --global user.email
```



```
git init
初始化git，生成.git目录(在mac下.git文件默认是隐藏的，可以在命令行使用open .git/来打开该目录)
```

```
git status
用来查看git下文件的状态
```

```
git add xxxx
将文件从untracked状态到staged状态

```

![屏幕快照 2018-09-03 14.41.08](../images/屏幕快照 2018-09-03 14.41.08.png)

