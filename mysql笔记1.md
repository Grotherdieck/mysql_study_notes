# 一、centos7下安装mysql

&emsp;&emsp;查看自己的mysql版本，安装与版本对应的mysql源，

```shell
cat /etc/redhat-release
```

&emsp;&emsp;然后去这个网站；http://repo.mysql.com/，找对应的版本，比如博主的是``7.9``，然后利用wget：

```shell
wget http://repo.mysql.com/mysql57-community-release-el7-9.noarch.rpm
/*el后面是对应的版本*/
```

&emsp;&emsp;然后把mysql新的yum源按到服务器上：

```shell
sudo rpm -Uvh mysql57-community-release-el7-9.noarch.rpm
```

&emsp;&emsp;然后就看到yum源有两个新的东西：

```shell
sudo ls /etc/yum.repos.d/
```

![](https://router-picture-bed.oss-cn-chengdu.aliyuncs.com/img/20220912172107.png)

&emsp;&emsp;接着yum安装mysql即可

```shell
sudo yum install -y mysql-community-server
```

