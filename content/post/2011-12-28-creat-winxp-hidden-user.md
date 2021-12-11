---
title: 在windowsXP中建立隐藏账户
date: '2011-12-28'
slug: 2011-12-28-creat-winxp-hidden-user
tags:
- 信息技术 INFORMATICS
- 转载 SHARE
- Windows
- XP
- 隐私
---


在XP中设置隐藏账户

所谓隐藏账户，是指不会显示在欢迎屏幕上，需要输入用户名和密码才可以进入。在公用计算机上建立隐藏账户是保护自己隐私的一个小伎俩。

设置隐藏账户的方法，先使用Administrator登录（可能需要进安全模式）：

1,“ 开始→运行”中输入并打开“cmd”。

2,输入“net user ABC 123
/add”这样就建立了一个名为“ABC”密码为“123”的受限制用户。

3,再输入“net localgroup administrators
ABC/add”将“ABC”的权限提升为管理员。

4,输入“regedit”打开注册列表。

5,在目录“HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows
NT\\CurrentVersion\\Winlogon\\
SpecialAccounts\\UserList”下建立一个与该目录下文件类型相同的文件并以刚才创建的用户“ABC”的名字“ABC”命名(如果已经存在该文件就不用再创建了)，再将参数改为“0”

6,这样就建立了一个隐藏用户。

7,最后再说以下，如果要删除这个隐藏用户就将那个参数改为“1”，再用“开始-运行”输入并打开“cmd”后输入“net
user ABC /del”这样一来就把用户“ABC”给删除了。
