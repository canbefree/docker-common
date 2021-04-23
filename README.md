docker-compose
==============


## mariadb

## elk

![](https://img.shields.io/badge/docker-kibana-green?style=plastic&logo=docker)
![](https://img.shields.io/badge/docker-elasticsearch-green?style=plastic&logo=docker)
![](https://img.shields.io/badge/docker-apmserver-green?style=plastic&logo=docker)

> kabana地址： https://localhost:5601

### 访问kibana  'Kibana server is not ready yet'
```
一般是elasticsearch没有启动，比如说：*max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]*

由于我的环境是 wsl,所以启动wsl 在  /etc/sysctl.conf 文件最后一行加上
vm.max_map_count=262144
```

## grafana

![](https://img.shields.io/badge/docker-grafana-green?style=plastic&logo=docker)

> grafana地址： http://localhost:3000

### 监控

- [X] etcd指标监控 https://etcd.io/docs/v3.4/metrics/
- [X] mysql指标监控 https://github.com/prometheus/mysqld_exporter
- [ ] redis指标监控

### prometheus指标查询
https://prometheus.io/

| 类型   | query                                                | 意义               |
| :----- | :--------------------------------------------------- | :----------------- |
| mysqld | mysql_global_status_commands_total{command="insert"} | insert 总数        |
| mysqld | rate(mysql_global_status_threads_connected[2m])      | 当前总连接数       |
| mysqld | mysql_global_status_threads_running                  | 正在运行的查询连接 |
| mysqld | mysql_global_status_aborted_connects                 | 拒绝连接数         |
| mysqld | mysql_global_status_connection_errors_total          | 服务器错误         |



