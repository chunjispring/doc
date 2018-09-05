# windows更换id

Teamviewer ID生成依据你电脑上的以下唯一属性：

- **网卡的mac地址**
- **硬盘的VolumeID**
- **Program Files文件夹的创建时间**

为了改变Teamviewer ID，你应该修改上面这三个值。

[TOC]

## 1.停止teamviewer运行

## 2.删除当前teamviewer在注册表中的ID

- For **Windows x86**, TeamViewer version [X], open *regedit.exe*, go to the branch HKLM\SOFTWARE\TeamViewer\Version[X] and delete DWORD value ClientID;
- For **Windows x64**, delete value ClientID from HKLM\SOFTWARE\Wow6432Node\TeamViewer\Version[X];
- Check if the registry key *HKEY_CURRENT_USER\Software\TeamViewer* exists and delete it.

## 3.改变Program Files文件夹的创建时间

下载[NirCMD](http://www.nirsoft.net/utils/nircmd.html),运行如下命令：

```
nircmdc.exe setfilefoldertime "C:\Program Files" now now
```

## 4.修改mac地址

打开cmd窗口运行如下命令：

```
ipconfig /all
```

注意 **Description**和**Physical Address**两个值

打开注册表，到HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e972-e325-11ce-bfc1-08002be10318}.

子目录有0000，0001......查找每一个分支中的**DriverDesc**,如果和ipconfig命令查出来的一致的话（我在计算机上发现自己的有两个都是一致的），新增或修改**REG_SZ**类型的名字为**NetworkAddress**的值，然后把想要修改的mac地址填写到该名称下面。

## 5.修改系统的VolumeID

VolumeID(Volume Serial Number)是硬盘分区的唯一标识。

下载[VolumeID](https://docs.microsoft.com/zh-cn/sysinternals/downloads/volumeid)

**以管理员权限打开CMD窗口**，运行：

```
vol
```

查看当前的volumeID，

改变当前的volumeID：

```
Volumeid.exe c: xxxx-xxxx
```

## 6.重启电脑

重启后，teamviewer的id就会发生改变（自己尝试第一次没有成功，又进行了一次上面的步骤就成功了）







