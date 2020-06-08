# InfluxDB.Notes

组件名称：couchdb 
安装文档：https://docs.influxdata.com/influxdb/v1.7/introduction/installation/
配置文档：https://docs.couchdb.org/en/latest/config/index.html
支持平台：Debian家族 | RHEL家族 | Windows | macOS | Docker

责任人：helin

## 概要

InfluxDB是一个由InfluxData开发的开源时序型数据库，由Go写成，着力于高性能地查询与存储时序型数据。InfluxDB被广泛应用于存储系统的监控数据，IoT行业的实时数据等场景。

## 环境要求

* 程序语言： go
* 应用服务器：
* 数据库:  
* 依赖组件：
* 其他：

## 安装说明

下面基于不同的安装平台，分别进行安装说明。

### CentOS

```shell
vi  /etc/yum.repos.d/influxdb.repo
[influxdb]
name = InfluxDB Repository - RHEL \$releasever
baseurl = https://repos.influxdata.com/rhel/\$releasever/\$basearch/stable
enabled = 1
gpgcheck = 1
gpgkey = https://repos.influxdata.com/influxdb.key
                                        #添加仓库

sudo yum -y install influxdb #安装influxdb

 #安装influxdb web gui: 采用官网下载rpm安装

sudo systemctl start influxdb chronograf
sudo systemctl enable influxdb chronograf
```

### Ubuntu

```
wget -qO- https://repos.influxdata.com/influxdb.key | sudo apt-key add -
source /etc/lsb-release
echo "deb https://repos.influxdata.com/${DISTRIB_ID,,} ${DISTRIB_CODENAME} stable" | sudo tee /etc/apt/sources.list.d/influxdb.list
sudo apt-get update && sudo apt-get install influxdb
sudo yum -y install influxdb #安装influxdb

sudo apt -y install chronograf  #安装influxdb web gui
sudo systemctl start influxdb chronograf
sudo systemctl enable influxdb chronograf
```



## 路径

* 程序路径：     /usr/lib/influxdb /etc/influxdb
* 日志路径：  /var/log/influxdb/influxd.log
* 配置文件路径   /etc/influxdb/influxdb.conf
* 启动路径:       /usr/bin/influx
* 其他...

## 配置

安装完成后，需要依次完成如下配置

```shell
vim /etc/influxdb/influxdb.conf
bind-address = "your ip:8083" 
```

## 账号密码

### 数据库密码

如果有数据库

* 数据库安装方式：
* 账号密码：

### 后台账号

如果有后台账号

* 登录地址 
* 账号密码    
* 密码修改方案：最好是有命令行修改密码的方案


## 服务

本项目安装后有服务,可设置为开机自启



```
 systemctl enable  influxdb                       
```

## 环境变量

列出需要增加的环境变量以及增加环境变量的命令：无

* 名称 | 路径

## 版本号

通过如下的命令获取主要组件的版本号: 

```
# Check influx version
influx -version 
```

## 常见问题

#### 有没有管理控制台？

1.1.0版本之后的没有管理控制台

http:// 公网 IP:8083即可访问

#### 本项目需要开启哪些端口？

| item | port |
| ---- | ---- |
| tcp  | 8086 |
| tcp  | 8088 |
| tcp  | 8083 |

#### 有没有CLI工具？

influx

## 日志

* 2020-05-12完成安装研究