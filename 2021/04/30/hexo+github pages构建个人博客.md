# Hexo大法好！！
经过一番折腾我终于折腾出来了！！

以下是我的hexo+github pages简易教程，网上已经有了很多教程，借鉴了比较多大佬的博客，这弄好了自己的博客，因为我认为每一篇有讲的详细的地方也有讲的不详细的地方，为了避免自己遗忘，写在这篇。
啊啊啊啊我恨为啥没有早点接触hexo，实在是太适合我这种菜鸡又想记东西的蒟蒻了！！

前提条件：git、node.js、hexo、GitHub账号
## 一、构建hexo静态博客步骤
我是按照我成功的步骤记录的，虽然中间有过失败的步骤，但是我没有及时记录，并且我的个人博客是重新建了两次才成功的。因此只记录下成功的步骤
##### 1.在你的目录下（如blog）右键git bash here
输入以下命令初始化hexo项目

```c
npm install -g hexo-cli
```
如图就是执行成功的界面
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191125224504750.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZvckFD,size_16,color_FFFFFF,t_70)
##### 2.hexo初始化，生成.git目录
输入以下命令进行初始化

```c
hexo init
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/2019112522495143.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZvckFD,size_16,color_FFFFFF,t_70)
##### 3.修改一下hexo的相关配置，比如博客名称啊之类的，然后就可以构建静态文件了
输入以下命令提交

```c
hexo g
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191125225049351.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZvckFD,size_16,color_FFFFFF,t_70)
提交成功之后就可以在本地查看啦，运行的命令：

```c
hexo s
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191125225207174.png)
## 二、在github的仓库生成github pages（利用git上传代码）
##### 1.先安装deployer
这里必须先安装这个才能后续的提交
否则会出现如下错误
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191125225640459.png)
```c
npm install hexo-deployer-git --save
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191125225420930.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZvckFD,size_16,color_FFFFFF,t_70)

##### 2.然后提交

```c
hexo g -d
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191125225620903.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZvckFD,size_16,color_FFFFFF,t_70)
我一开始也是最后遇到的问题，唉，纠结的最久的地方就是密钥问题了，这里他让我输入密码，我没有输入，默认没有密码，结果报错了
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191125230021397.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZvckFD,size_16,color_FFFFFF,t_70)
我再执行了一次就莫名的行了，但是这次我输入了密码，是github账号的密码，应该是行得通的，下面是成功之后的
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191125230147757.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZvckFD,size_16,color_FFFFFF,t_70)

好像我有一个问题没有提到，就是ssh密钥问题，但是这个是之前git和github互通的时候设置的了，ssh只要设置一个就可以了，它好像自己会识别，这个我也不是很懂啦- -

暂时先这样吧，像师兄说的hexo个人博客弄起来四个小时就够了，我前面弄了总共八个小时吧，因为中间报错之类的，一报错就没得办法，就是自己折腾，折腾着折腾着就出来了

啊还有一个很方便的东西，就是上述步骤完成之后，想要完善自己的个人博客可以到hexo官网看教程，关于发表文章（hexo上叫做日志），有一个超级无敌方便的办法，就是直接导出.md文件，然后把.md文件直接复制到source/_post下，然后再执行一次

```c
hexo g
```
然后就会给新加入的.md文件生成静态文件，在博客中呈现
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191125230730483.png)
