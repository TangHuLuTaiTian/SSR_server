SSR服务端部署与使用
========

### 市面上的SSR服务端版本太多，由于本项目是公司使用，所以需要搭配后台。挑选之下，选用了开源项目[SSR](https://github.com/ouhaohan8023/SSR_server)与[SSRPanel](https://github.com/ouhaohan8023/shadow.com)
### [博客地址](http://www.ohh.ink/#/novel?id=30)
### [Github](https://github.com/ouhaohan8023/SSR_server)
### 在此，衷心感谢作者：
### 1. [Bruskyii Panda](https://github.com/ssrpanel)

### 因为站在巨人的肩膀上才有的此项目，谢谢各位的奉献！

### 由于本项目是搭配后台使用的，数据存储再数据库，所以本项目无法单独运行（如果你会改配置那就没有什么不可以！）。所以，再使用本项目前，请搭建后台，[传送门](https://github.com/ouhaohan8023/shadow.com)

### 后台客户端展示[需要先安装后台](https://github.com/ouhaohan8023/shadow.com)
![client](https://github.com/ouhaohan8023/shadow.com/raw/master/pre/client.png)

### 后台管理员展示[需要先安装后台](https://github.com/ouhaohan8023/shadow.com)
![server](https://github.com/ouhaohan8023/shadow.com/raw/master/pre/admin.png)

### 本项目为服务端，使用方法如下：
0. 首先安装本项目对应的后台[传送门](https://github.com/ouhaohan8023/shadow.com)
1. git clone https://github.com/ouhaohan8023/SSR_server.git
2. cp config.json user-config.json
3. cp apiconfig.py userapiconfig.py
4. cp mysql.json usermysql.json
5. 修改对应的数据库配置参数
6. 回到根目录，运行`python server.py`，查看输出信息（为了保证这一步的输出信息比较完整，请提前再后台用随机生成用户功能，生成一些测试用户）
>`python server.py`示例如下：
>1. 运行后会展示账户信息（在后台配置）
> ![账户信息](https://github.com/ouhaohan8023/shadow.com/raw/master/pre/shell1.png)
>
>2. 使用过程中展示TCP信息
> ![TCP](https://github.com/ouhaohan8023/shadow.com/raw/master/pre/shell2.png)

### 调试完毕，正式运行
1. 根目录下运行`./run.sh`(无日志)
2. 需要日志的话运行`./logrun.sh`

### 常见问题
>1.VPS重启以后，经常会出现，后台显示上线，但是客户端连接上以后无法打开网页，并且没有流量。
>
>解决方法：运行`systemctl stop firewalld`或者`systemctl stop iptables.service`停止防火墙。