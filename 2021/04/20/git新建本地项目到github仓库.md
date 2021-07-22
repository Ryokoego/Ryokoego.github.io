# git死亡入门
1.先在GitHub上创建仓库以及
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191123235133204.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZvckFD,size_16,color_FFFFFF,t_70)
2.创建密钥
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191123235227713.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZvckFD,size_16,color_FFFFFF,t_70)
3.先进入git，先进入新建项目目录

```c
cd 目录/目录
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191123234941446.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZvckFD,size_16,color_FFFFFF,t_70)
4.然后可以看到生成一个文件夹
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191123235347424.png)
5.将需要上传的代码目录复制到这个目录下
6.然后在这个目录下右键“git bash here”弹出git图形界面
执行三步

```c
git add .
git commit -m '描述'
git push
```
最后push就完成了上传，去GitHub新建的仓库查看
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191123235708202.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZvckFD,size_16,color_FFFFFF,t_70)
每一次对文件进行修改就到终端目录下面git bash here执行git push就可以上传了，回退之类的操作还没有学到，再说吧
