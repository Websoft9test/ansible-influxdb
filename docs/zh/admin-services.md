# 服务启停

使用由Websoft9提供的 InfluxDB 部署方案，可能需要用到的服务如下：

## InfluxDB

```shell
sudo systemctl start Influxdb-server
sudo systemctl stop Influxdb-server
sudo systemctl restart Influxdb-server
sudo systemctl status Influxdb-server

# you can use this debug mode if InfluxDB service can't run
Influxdb-server console
```

### MySQL

```shell
sudo systemctl start mysql
sudo systemctl stop mysql
sudo systemctl restart mysql
sudo systemctl status mysql
```

### Redis

```shell
systemctl start redis
systemctl stop redis
systemctl restart redis
systemctl status redis
```