# avip_ITS
List of ITS papers

###Basic

本list主要是存放大家查找和看过的论文基本信息，以最大程度上避免看其他人筛选过的论文

基本格式如下
>年份，打分，论文title, 作者    
2010，5，Traffic State Estimation using Traffic Data from Fixed Detectors and Probe Vehicles, ApprenticeZ

打分范围1-5，根据个人的理解评价其相关程度，有利于其他人找到同样的文章时参考是否选择阅读，通常来讲，打5分表示自己选定这篇文章了，最好避免打4分。

**建议大家遵循“少量多次”的原则更新survey list，便于其他小伙伴及时了解动态，也减轻merge操作的压力. **

###Git
需要安装本地Git版本管理，安装后第一次需要进行简单配置，我发现可以直接在github上在线编辑，然后提交本次编辑的修改，貌似也行，可以试试。不过本次顺便熟悉一下使用git也是极好的。

```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

切到目标文件夹目录下，拉取远程文件，执行
```sh
git clone https://github.com/imerse/avip_ITS.git
```
每次要自己要编辑list文件之前都执行 
```sh
git pull —-rebase origin master
```
如果提示有confilct，需要先打开文件，会有三行类似 

> "=================HEAD"<br/>
> "==================="<br/>
> "===================[本次的提交编号]"


此时表示在你当前编辑的时候，别人同时编辑并push了，只需要简单Check一下上面三行之间的[文章]内容有没有重复，没有的话就直接删掉这三行，然后继续执行下面的命令；有重复表示你们同时找了相同的文章，嗯，私下解决删掉谁的，^_^。

编辑完成之后   
```sh
git add .  //将所有的更改增至索引   
git commit -am “message”   //message为本次改动的一个tag，可随意   
```
push到远程的分支
```sh
git push origin local_branch:master  //local_branch通常为master，如果没有特别设置过，直接用master就可以 
```
Done.
