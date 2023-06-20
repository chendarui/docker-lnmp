# docker-lnmp

docker集成环境包含服务
> 按需对docker-compose.yml文件里面的服务释放注释进行安装
- Nginx
- PHP7.4
- PHP8
- Mysql
- Openresty
- Redis
- Memcached
- rabbitmq
- mongodb
- elasticsearch
- supervisor

文件夹目录说明
- data(各服务数据文件)
- logs（日志目录。可在编排文件中设置服务的日志映射）
- services（服务配置文件等）
- www（项目代码）

常用docker-compose命令

```
【启动服务】
docker compose up [SERVICE...]
例子：
docker compose up mysql -d(后台运行myqsl)
选项：
-d：在后台运行服务容器。
–no-deps：不启动服务所依赖的其他服务（由depends_on元素指定）。
–no-color：不使用颜色来区分不同服务的控制台输出。
–force-recreate：总是重新创建容器，不能与 --no-recreate 同时使用。
–no-recreate：如果容器已经存在了，则不重新创建，不能与 --force-recreate 同时使用。
–no-build：不进行服务镜像的构建，即使该服务镜像不存在。
-t, --timeout TIMEOUT：停止容器时的超时时间（默认为 10 秒）。
–scale：设置某个服务要启动的容器数量，用于快速扩容/缩容，例如 --scale='web=3' 将为web服务启动3个容器副本，并且会覆盖docker-compose.yml中原有的 scales设置。
```

```
【停止服务】
docker compose stop [SERVICE...]
例子：
docker compose stop mysql
```