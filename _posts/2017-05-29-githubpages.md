---
layout: post
title: 如何在Github Pages搭建自己写的页面
categories: Github Pages
description: Github Pages
keywords: Github Pages
---

开始教程之前的准备工作：

1、需要你自己写的网页文件。

![](https://ooo.0o0.ooo/2017/07/03/595a10f1d784a.png)

2、注册Github。

3、下载安装git。下载地址https://git-scm.com/downloads

教程开始：（以下出现的test指你的网页名或者你想起的一切名字）

> 步骤一：登录到Github上，新建一个repo，命名为test，勾选 initialize this repository with a README，点击create repository。

![](https://ooo.0o0.ooo/2017/07/03/595a1132b1dad.png)

![](https://ooo.0o0.ooo/2017/07/03/595a1154788c9.png)

> 步骤二：打开settings，有一个Github Pages 的设置，点击 source 中的本来的 None ，使其变成 master 分支，也就是作为部署github pages 的分支，然后点击 save。

![](https://ooo.0o0.ooo/2017/07/03/595a1195c7a88.png)

> 步骤三：页面刷新之后，再看 github pages 设置框处，多了一行网址，就是你的 github pages 的网址了。

![](https://ooo.0o0.ooo/2017/07/03/595a11bf95942.png)

点击这个链接

![](https://ooo.0o0.ooo/2017/07/03/595a11ddaffaf.png)

好了，别激动了，真正让一个小白你发疯的阶段开始了，有了自己的网址，但页面显示的是什么鬼？

至此以上，github上要处理的操作告一段落，该上Git了！

> 步骤四 ：打开此电脑，选择一个盘，比如 f 盘，右键空白处点击 git bash here。

![](https://ooo.0o0.ooo/2017/07/03/595a120082c75.png)

> 步骤五：输入如下命令，用来在 f 盘创建 test 文件放你的github上的test repository，克隆test repository到 test 文件中。
![](https://ooo.0o0.ooo/2017/07/03/595a1228e5284.png)

这个时候你的 f 盘，就会多一个 test 文件，打开它，
![](https://ooo.0o0.ooo/2017/07/03/595a124897725.png)

会看到一个 README.md 的文件，这个文件是从哪来的呢？追溯到gihub上，你会发现 README 文件是来自 master 分支。
![](https://ooo.0o0.ooo/2017/07/03/595a12694300a.jpg)

> 步骤六： 将自己的网页文件复制粘贴至 f 盘的 test 文件中

![](https://ooo.0o0.ooo/2017/07/03/595a128fa20bf.png)

> 步骤七：执行如下命令

![](https://ooo.0o0.ooo/2017/07/03/595a12c06ae40.png)

![](https://ooo.0o0.ooo/2017/07/03/595a13001ad79.png)

解释一下上面的命令：首先输入  git status   列出当前目录所有还没有被git管理的文件和被git管理且被修改但还未提交(git commit)的文件，也就是所有改动文件，红色字体标出。

然后输入 git add .  (有个点) 表示添加当前目录下的所有文件和子目录，

然后 再输入一次 git status 如果看见文件都变绿了 ，那么就代表 它们已经准备好了被提交（git commit）。



> 步骤八：输入如下命令，将你的文件上传至远程 master 分支

![](https://ooo.0o0.ooo/2017/07/03/595a132e2f49e.png)

![](https://ooo.0o0.ooo/2017/07/03/595a13528107b.png)

输入最后一行 git push，按回车，等一会，会有弹出框让你输入你的 github 账号和密码。

![](https://ooo.0o0.ooo/2017/07/03/595a13885cb2c.png)

![](https://ooo.0o0.ooo/2017/07/03/595a1398cdb89.png)

ok之后耐心等待。

当出现像下图中的语句之后，你已经完成了99%。
![](https://ooo.0o0.ooo/2017/07/03/595a13c4714f1.png)

> 最后一步：打开浏览器输入给你的网址加上你上传的 html 文件名 test.html，然后重重的按下回车。

![](https://ooo.0o0.ooo/2017/07/03/595a13e440861.png)

恭喜你，成功了！！！

参考网址：[http://www.cnblogs.com/lijiayi/p/githubpages.html](http://www.cnblogs.com/lijiayi/p/githubpages.html)
