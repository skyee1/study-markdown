### 安装
参考菜鸟教程

### 查看拥有的本地镜像
`
docker images
`

### 启动镜像（开机）
`
docker run -itd --name ubuntu-test ubuntu
`

### 查看运行信息
`
docker ps
`

### 进入镜像
`
docker exec -it ubuntu-test /bin/bash
`
