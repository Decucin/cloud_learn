1. 安装docker
2. docker安装mysql
````shell
docker pull mysql
````
    运行mysql
````shell
docker run -p 3306:3306 --name mysql \
-v /mydata/mysql/log:/var/log/mysql \
-v /mydata/mysql/data:/var/lib/mysql \
-v /mydata/mysql/conf:/etc/mysql \
-e MYSQL_ROOT_PASSWOED=root \
-d mysql
````
3. 安装redis
````shell
docker pull redis
````
````shell
docker run -p 6379:6379 --name redis \
-v /mydata/redis/data:/data \
-v /mydata/redis/conf/redis.conf:/etc/redis/redis.conf \
-d redis redis-server /etc/redis/redis.conf
````
4. 创建项目
5. 