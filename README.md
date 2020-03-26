# Docker Centos Nginx

## 环境

```
centos: ^7
nginx: openresty-1.15.8.2
```

## 常用命令：

```sh
# 拉取镜像
$ docker pull hollisho/nginx

# 运行；若配合 php 使用，注意 <html-dir> 和 <tmp-dir> 与 php 一致
$ docker run --name nginx-test -d -p 80:80 -p 443:443 -v <conf-dir>:/usr/local/openresty/nginx/conf/conf.d hollisho/nginx

# 例子：
$ docker run --name nginx-alias1 -d -p 80:80 -p 443:443 -v /etc/nginx/conf.d:/usr/local/openresty/nginx/conf/conf.d hollisho/nginx

# 查看正在运行的容器
$ docker ps

# 停止
$ docker stop [CONTAINER ID | NAMES]

# 启动
$ docker start [CONTAINER ID | NAMES]

# 进入终端
$ docker exec -it [CONTAINER ID | NAMES] sh

# 删除容器
$ docker rm [CONTAINER ID | NAMES]

# 镜像列表查看
$ docker images

# 删除镜像
$ docker rmi [IMAGE ID]
```
