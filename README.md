docker-compose 
====================


## mariadb
[![](https://img.shields.io/badge/docker-mariadb-green?style=plastic&logo=docker)](https://hub.docker.com/_/mariadb)
[![](https://img.shields.io/badge/github-mariadb-green?style=plastic&logo=github)](https://github.com/MariaDB/mariadb-docker)


## elk
![](https://img.shields.io/badge/docker-kibana-green?style=plastic&logo=docker)
![](https://img.shields.io/badge/docker-elasticsearch-green?style=plastic&logo=docker)
![](https://img.shields.io/badge/docker-apmserver-green?style=plastic&logo=docker)


> kabana地址： https://localhost:5601

### 访问kibana  'Kibana server is not ready yet'

一般是elasticsearch没有启动，比如说：*max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]*

由于我的环境是 wsl,所以启动wsl 在  /etc/sysctl.conf 文件最后一行加上
vm.max_map_count=262144


### 如何添加mysql 指标
参考：http://localhost:5601/app/home#/tutorial/mysqlMetrics


## grafana 
![](https://img.shields.io/badge/docker-grafana-green?style=plastic&logo=docker)

> grafana地址： http://localhost:3000

### 如何添加etcd监控
已实现，请本项目etcd部分

### 如何添加mysql 监控


