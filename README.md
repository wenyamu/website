## 创建镜像命令
```
docker build -t diy:1 .
```

## edit from https://github.com/dockette
## 注意 buster 与 bullseye 在安装 php 模块时名称的不同之处
> for buster
```
FROM dockette/debian:buster
......
RUN apt install -y --no-install-recommends \
  php7.4-apc \
  php7.4-mongo \
  ......
......
```
> for bullseye
```
FROM dockette/debian:bullseye
......
RUN apt install -y --no-install-recommends \
  php7.4-apcu \
  php7.4-mongodb \
  ......
......
```
