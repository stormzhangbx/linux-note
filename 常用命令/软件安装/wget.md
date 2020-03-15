# wget命令

使用时如果没有指定-P，那么下载项默认存放再当前目录。如，用root账户登录Linux服务器，刚登录进入的是`~`目录，即`/root`目录。此时执行

```sh
[root@ecs-s6-medium-2-linux-20200125191715 ~]# wget http://download.redis.io/releases/redis-5.0.7.tar.gz
```

下载完成后`/root/`目录下会多出一个redis-5.0.7.tar.gz压缩包
