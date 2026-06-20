---
title: 我的blog
abbrlink: 381c36c9
date: 2024-11-03 17:47:13
tags:
cover: /img/ziluolan.png
---
<font style="color:rgb(89, 99, 110);">参考文章：</font>[如何用Hexo搭建个人博客?](https://blog.fiveth.cc/p/bb32/)  

[Windows系统Git安装教程（详解Git安装过程） - 学为所用 - 博客园](https://www.cnblogs.com/xueweisuoyong/p/11914045.html)

[NPM express模块本地安装和全局安装详解_npm install express -g-CSDN博客](https://blog.csdn.net/qq_27278957/article/details/77175651)

[Hexo博客搭建基础教程(一) | Fomalhaut🥝](https://www.fomal.cc/posts/e593433d.html)

[Node.js安装及环境配置之Windows篇 - 刘奇云 - 博客园](https://www.cnblogs.com/liuqiyun/p/8133904.html)

<h1 id="O1q75"><font style="color:rgb(31, 35, 40);">一. 准备工作</font></h1>
<h2 id="czb3N">GitHub</h2>
1、下载[steam++](https://steampp.net)和uu加速器,对github加速(如果会魔法的话，就没必要下载）

注：GitHub运营在国外，经常会很卡。访问网页推荐用steam++，但之后有一步必须将steam++关闭换成uu加速器。有人说校园网访问外网效果会好点。![](https://cdn.nlark.com/yuque/0/2024/png/50077463/1730565882952-96459fe6-f4f6-4e8b-a4c7-559d28d10dff.png)



![](https://cdn.nlark.com/yuque/0/2024/png/50077463/1730565857728-aa5a1a2f-53a8-483f-ba68-71a96d93a949.png)

2、<font style="color:rgb(31, 35, 40);">注册一个</font>[GitHub](https://github.com/)<font style="color:rgb(31, 35, 40);">账号</font>

<h2 id="zF9v1"><font style="color:rgb(0, 0, 0);">Node.js</font></h2>
官网：[Node.js — Run JavaScript Everywhere](https://nodejs.org/en)

_<font style="color:rgb(0, 0, 0);">(这篇文章里有修改nodejs缓存路径的教学:</font>_[_<font style="color:rgb(0, 0, 0);">文章链接</font>_](https://www.cnblogs.com/liuqiyun/p/8133904.html)_<font style="color:rgb(0, 0, 0);">，c盘战士可以不看)</font>_

_<font style="color:rgb(0, 0, 0);">关于express的部分</font>_[NPM express模块本地安装和全局安装详解_npm install express -g-CSDN博客](https://blog.csdn.net/qq_27278957/article/details/77175651)讲的上面的更详细

<h2 id="cy2r2">[git](https://git-scm.com/book/zh/v2/%E8%B5%B7%E6%AD%A5-%E5%AE%89%E8%A3%85-Git)</h2>
官网下载，即可

**<font style="color:rgb(0, 0, 0);">接下来我们测试下是否都下载成功</font>**

<font style="color:rgb(0, 0, 0);">win+R，输入cmd，依次输入</font>

```plain
node -v
npm -v（这个是node附带的）
git -v
```

结果如下

![](https://cdn.nlark.com/yuque/0/2024/png/50077463/1730565340533-855ab0d9-3431-4717-96dd-e3acffb6b296.png)

<h2 id="uVkvF">**<font style="color:rgb(0, 0, 0);">下载hexo</font>**</h2>
在cmd里继续输入下面这行代码

| ```plain npm install hexo-cli -g ```  |
| --- |


<h1 id="Ivb9y"><font style="color:rgb(31, 35, 40);">二. 搭建仓库</font></h1>
可参考【【零成本】Hexo个人博客搭建教程 | 无需服务器】 [https://www.bilibili.com/video/BV1Ju4m1c7WR/?share_source=copy_web&vd_source=ddecc3757057954ae503b10eae9a1c8e](https://www.bilibili.com/video/BV1Ju4m1c7WR/?share_source=copy_web&vd_source=ddecc3757057954ae503b10eae9a1c8e)

<font style="color:rgb(31, 35, 40);">这里就要用到我们之前注册的GitHub账号。</font>

<font style="color:rgb(31, 35, 40);">Create repository</font>

![](https://cdn.nlark.com/yuque/0/2024/png/50077463/1730566080993-cd839e17-5858-4b73-b9e2-78f295c2790e.png)

![](https://camo.githubusercontent.com/f15c019d8a990aa7070f7af412711bc18a46daa96ce145f20e5830754d1c2743/68747470733a2f2f63646e2e6e6c61726b2e636f6d2f79757175652f302f323032342f706e672f34323535343737342f313733303236323731303037342d61303732656337622d616230352d343933362d626239382d3662336362653537623834392e706e67)

<font style="color:rgb(31, 35, 40);">仓库名必须按照格式填写，即：</font>**<font style="color:rgb(31, 35, 40);">用户名.github.io</font>**

<font style="color:rgb(31, 35, 40);">必须是public</font>

<font style="color:rgb(31, 35, 40);">Add a README file打勾</font>

<h1 id="ji076"><font style="color:rgb(31, 35, 40);">三. 配置ssh key</font></h1>
1. <font style="color:rgb(31, 35, 40);">在桌面空白处右键，点显示更多选项，打开git bash，粘贴下面这串代码，记得把邮箱改成自己的，然后敲四下键盘</font>

```plain
ssh-keygen -t rsa -C "邮件地址"
```

2. <font style="color:rgb(31, 35, 40);">之后就去C盘用户文件夹里的某个文件夹里去找下面这个文件夹  
</font>![](https://camo.githubusercontent.com/04bc9cdb4795ccdee239ab8dcd864b5e4a6cf174f4124e1a103912833c2c13f1/68747470733a2f2f63646e2e6e6c61726b2e636f6d2f79757175652f302f323032342f706e672f34323535343737342f313733303236333733373730302d61633231383063342d386264362d343166362d626331642d3939636234653166363265652e706e67)<font style="color:rgb(31, 35, 40);">  
</font><font style="color:rgb(31, 35, 40);">点开里面找到id_rsa.pub打开（使用word打开就行），全选复制</font>
3. <font style="color:rgb(31, 35, 40);">GitHub，打开Settings</font>

![](https://cdn.nlark.com/yuque/0/2024/png/50077463/1730566584354-dd534660-58aa-403b-b5d7-b67fce2406e5.png)

找到ssh key，创建新的![](https://cdn.nlark.com/yuque/0/2024/png/50077463/1730566629955-8e134da5-55ee-4975-98c7-1a32b4c4a1d3.png)

![](https://cdn.nlark.com/yuque/0/2024/png/50077463/1730566688985-d2ba5e90-ddcf-45d7-a3ea-5ec3fa30e329.png)<font style="color:rgb(31, 35, 40);">  
</font><font style="color:rgb(31, 35, 40);">title随便起，key就是刚刚复制的那一段代码</font>

4. <font style="color:rgb(31, 35, 40);">回到桌面，打开git bash，输入下面这串代码，验证一下有没有添加成功</font>

```plain
ssh -T git@github.com
```

<font style="color:rgb(31, 35, 40);">回车后记得输入yes</font>

<font style="color:rgb(31, 35, 40);">注：到这必须关闭steam++</font>

![](https://cdn.nlark.com/yuque/0/2024/png/50077463/1730621410044-322fef40-d88a-4d82-b081-43fc6deef932.png)

<h1 id="uqLYi"><font style="color:rgb(31, 35, 40);">四. 本地部署</font></h1>
1. <font style="color:rgb(31, 35, 40);">创建一个文件夹，用来放置博客文件</font>![](https://cdn.nlark.com/yuque/0/2024/png/50077463/1730621555203-8b3ed798-ed9f-41ec-b1e7-c493b09089c4.png)
2. <font style="color:rgb(31, 35, 40);">打开文件夹，打开git bash对文件夹进行初始化，依次输入以下代码</font>

:::info
<font style="color:rgb(31, 35, 40);">npx hexo init</font>

:::

安装

:::info
<font style="color:rgb(31, 35, 40);">npx hexo install</font>

:::

<font style="color:rgb(31, 35, 40);">生成</font>

:::info
<font style="color:rgb(31, 35, 40);">npx hexo g</font>

:::

本地部署

:::info
<font style="color:rgb(31, 35, 40);">npx hexo s</font>

:::

<font style="color:rgb(31, 35, 40);">这之后我们就会得到一个链接，打开就可以看到我们的博客在本地部署啦，这就是我们的博客了，这里记得回到命令行点ctrl+c停止本地服务器，然后再关闭窗口</font>

<font style="color:rgb(31, 35, 40);">由于github服务器在国外，这里建议使用uu加速器里面的学术资源模块进行加速</font>

<h1 id="pvp9M"><font style="color:rgb(31, 35, 40);">五. 上线博客</font></h1>
到这里上面那个B站视频由于剪辑失误，缺少一部分东西，之后的可以参考[https://www.fomal.cc/posts/e593433d.html](https://www.fomal.cc/posts/e593433d.html)

1. <font style="color:rgb(31, 35, 40);">首先用记事本打开博客文件夹里的下面这个文件</font>

![](https://cdn.nlark.com/yuque/0/2024/png/50077463/1730622270367-a85ba4c6-7d8d-4317-b474-06d2fb2e7884.png)

2. <font style="color:rgb(31, 35, 40);">拖到最底下，把deploy后面的全删掉，复制粘贴下面这段（注意缩进）</font>

<details class="lake-collapse"><summary id="u3f855a16"></summary><p id="ue4041bd9" class="ne-p"><span class="ne-text">deploy:</span></p><p id="uec026c91" class="ne-p"><span class="ne-text">    type: git</span></p><p id="u88f905bf" class="ne-p"><span class="ne-text">    repository: git@github.com:user name/user name.github.io.git</span></p><p id="ucac2b040" class="ne-p"><span class="ne-text">    branch: main</span></p></details>
3. <font style="color:rgb(31, 35, 40);">然后桌面打开git bash，依次输入</font>

:::info
npm install hexo-deployer-git --save

:::

:::info
+ <font style="color:rgb(31, 31, 31);">npx hexo generate：生成静态文章，可以用</font>`<font style="color:rgb(244, 116, 102);">hexo g</font>`<font style="color:rgb(31, 31, 31);">缩写</font>
+ <font style="color:rgb(31, 31, 31);">npx hexo deploy：部署文章，可以用</font>`<font style="color:rgb(244, 116, 102);">hexo d</font>`<font style="color:rgb(31, 31, 31);">缩写</font>

:::

<font style="color:rgb(31, 31, 31);">因为第一次使用。需要写入自己的邮箱和用户名</font>

:::info
<font style="color:rgb(31, 31, 31);">git config --global user.email "你的邮箱"</font>

<font style="color:rgb(31, 31, 31);">git config --global user.name "你的名字"</font>

:::

<font style="color:rgb(0, 0, 0);">配置完后再</font>`hexo d`<font style="color:rgb(0, 0, 0);">上传</font>

<font style="color:rgb(0, 0, 0);">在跳出来的窗口内进行登录</font>

<font style="color:rgb(0, 0, 0);">接下来我们就成功把本地内容上传到github了</font>

<font style="color:rgb(0, 0, 0);">上传成功以后，我们就算搭建好了！上自己的网址看看吧</font>

<font style="color:rgb(0, 0, 0);">网址是我们之前设的仓库名：用户名.github.io</font>

