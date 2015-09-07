# mysql
mysql 5


可以使用 MYSQL_DATABASE 参数指定运行容器之前就创建名为 wordpress 的数据库：

docker run --name wordpressdb -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=wordpress -d mysql:5.7
当然，MySQL 数据库还有其他的参数，例如指定创建用户和密码。当然，更多的用法就需要参考他们 官方的文档 了。

容器的 IP 会随启动而变化，需要使用 docker inspect --format='{{.NetworkSettings.IPAddress}}' wordpressdb 获取容器的 IP。
