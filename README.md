## edit from https://github.com/dockette

## 创建镜像命令
```
docker build -t diy:1 .
```

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

## bullseye 使用的是 tengine 并且安装了扩展
## buster 使用的是原版 nginx 并未安装扩展
