# redis
#redis在linux下面的安装使用
redis 学习笔记和用法

1.redis-cli -h 127.0.0.1 -p 6379 
使用制定Ip和端口的方式链接redis，这里-h如果不指定，则默认为127.0.0.1，-p不指定则默认为6379

2.redis-cli shutdown save|nosave 
发出命令关闭redis，并且通过参数指定是否将数据持久化到文件中。
这里需要注意的是，我们也可以通过kill命令来关闭redis，这种情况redis也会生成持久化文件；但是不要用过kill -9强制关闭reids，
此时redis不会生成持久化文件，极端情况下会造成aof文件和复制数据丢失的问题
