##说明
这个项目是从[powergx](https://git.airl.us/powergx)的[Crysadm](https://git.airl.us/powergx/crysadm)项目fork来的。原项目的目的是构建一个web版本迅雷赚钱宝的监控平台。因为我没有服务器，所以我做了这个docker镜像部署项目，使用[DaoCloud](https://www.daocloud.io/)提供的免费Docker容器来运行(二级域名也挺好的哦~~)。


##非常惭愧
github的帐号很久以前就注册了，但是没有好好利用。总是三天打鱼两天晒网，这是第一次正真意义上使用github平台，所以有做的不对的地方，请各位客官见谅。

##部署
赚钱宝的主人们可以无偿使用这套代码来部署属于自己的监控平台。对软件部署不懂的朋友，我调试好容器后，会做一个DaoCloud平台注册和使用教程，到时候我会将我做的镜像公布出来，方便大家使用。

##感谢
在此特别感谢[powergx](https://git.airl.us/powergx)同学，感谢他的无私奉献精神，让我们有这么好的web监控体验。谢谢！

##powergx：
运行环境 python3.3+ , redis
* crysadm 启动web服务
* config 配置redis server
* crysadm_helper 启动后台服务

安装后访问 /install 生成管理员账号
config.py.example 改名为config.py 使用

##补充说明
最近有几位同学询问怎么配置不成功，在这里补充说明一下详细细节。ps：已经有同学在vps上配置成功并且正常使用了。
* 把config.py文件删掉，然后将config.py.example文件重命名为config.py，然后在这个文件中修改你们自己的具体配置信息。
* 注意满足python的requirements.txt依赖，使用命令：pip install -r requirements.txt安装；
* 注意服务端口默认是5000，所以你访问的时候应该访问xxx.xxx.xx.x:5000，你也可以修改为80端口，如果你的服务器80端口正好闲置的；
* 启动服务后，第一次访问xx.xx.xx.x:5000/install地址，注意是install结尾的，用来生成管理员账号和密码；
* 如果在启动服务器看到有错误提示，不要着急，尝试下能不能正常访问web页面，如果可以正常访问的话，那就不要在意这些错误了……^_^……

