#redis搭建


###### 1,OneMasterTwoSlave-一主两从

master端口:6379

相关启动命令:
`./redis-server redis6379.conf`

bake1端口:6380
相关启动命令:
`./redis-server redis6380.conf`

bake2端口:6381
相关启动命令:
`./redis-server redis6381.conf`

总结:`1:主从区别,从机写连接主机所需密码`
    `2:slaveof 49.235.115.4 6379`

###### 2,OneMasterTwoSlaveThreeSentinel-一主两从三哨兵(基于一主两从进行搭建)

区别:port配置

运行后,sentinel***.conf最底部会写入相关哨兵配置