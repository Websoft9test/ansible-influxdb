# Start or Stop the Services

These commands you must know when you using the InfluxDB of Websoft9

## InfluxDB

```shell
sudo systemctl start influxdb-server
sudo systemctl stop influxdb-server
sudo systemctl restart influxdb-server
sudo systemctl status influxdb-server

# you can use this debug mode if InfluxDB service can't run
influxdb-server console
```

## InfluxDB

```shell
sudo systemctl start influxdb-server
sudo systemctl stop influxdb-server
sudo systemctl restart influxdb-server
sudo systemctl status influxdb-server

# you can use this debug mode if InfluxDB service can't run
influxdb-server console
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