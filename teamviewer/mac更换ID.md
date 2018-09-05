# MAC系统下解决Teamviewer 5 分钟限制

网上找了好久，尝试和其他软件一样找破解版的，结果找的各种都是假的，根本不是破解版。最终找到解决方案，**改变Teamviewer客户端的ID**。

[TOC]



## 1.关闭Teamviewer

## 2.下载 [TeamViewer-id-changer.py](https://gist.github.com/zhovner/b1d72f3465c46e7b58a4ea42d625c3e8#file-teamviewer-id-changer-py)

[Teamviewer本地地址](../files/TeamViewer.dmg)

[python脚本本地地址](../files/TeamViewer-id-changer.py)

运行脚本文件







 

## 3.运行脚本文件

```
sudo python Downloads/TeamViewer-id-changer.py
```

上面Downloads是我电脑上的脚本存放位置，具体运行时视情况而定。

## 4.重启电脑

## 5.重新打开Teamviewer

若上述操作成功，便会发现此时的Teamviewer客户端的ID已经发生了变化。否则可以多尝试几次。若还是不行，那可能这个方案并不适合你的电脑。