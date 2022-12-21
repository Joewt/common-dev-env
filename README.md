# docker 开发环境  

## 前置
首先安装docker 和 docker-compose  

## 启动
一键启动环境  
docker-compose up -d  


docker-compose up -d nginx                构建建启动nignx容器  

docker-compose exec nginx bash            登录到nginx容器中  

docker-compose ps                         显示所有容器  

docker-compose restart nginx              重新启动nginx容器  

docker-compose build nginx                构建镜像 。  

docker-compose build --no-cache nginx     不带缓存的构建。  

docker-compose logs  nginx                查看nginx的日志  

docker-compose logs -f -tail 100 nginx              查看nginx的实时日志  

docker-compose events --json nginx        以json的形式输出nginx的docker日志  

docker-compose pause nginx                暂停nignx容器  

docker-compose unpause nginx              恢复ningx容器  

docker-compose stop nginx                 停止nignx容器  

docker-compose start nginx                启动nignx容器  



## 注意事项


### mysql8

需要更新下远程登录权限
```

ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';

update user set host = '%' where user ='root';

FLUSH PRIVILEGES;

```