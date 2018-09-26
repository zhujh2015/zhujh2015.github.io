### 1.远程链接到服务器
redis-cli -h 127.0.0.1-p 6379
### 2.获取所有keys 
keys *
### 3.一定条件检索
keys *abcd*
### 5、 清空所有数据库的所有 key
   flushall
### 6、命令用于清空当前数据库中的所有 key。
   FLUSHDB
### 7、查找库
    select 1  
### 8、根据key 进行删除
    DEL KEY_NAME