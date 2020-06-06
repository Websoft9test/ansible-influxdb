# Troubleshooting

We collect the most common troubleshooting of using InfluxDB for your reference:

> Instance troubleshooting is closely related to the Instance provider that is Cloud Platform, refer to [Cloud Platform Documentation](https://support.websoft9.com/docs/faq/tech-instance.html)

#### How can I use the logs?

You can find the keywords **Failed** or **error** from the logs directory: `/data/logs`

#### InfluxDB service can't start?

1. Use the debug mode of `influxdb-server console` and you can see the errors
   ```
   influxdb-server console
   ```
2. Search the keywords **Failed** or **error** from logs: */data/logs/influxdb-server*

#### Error in Chrome when modify password?

This error is not attribute to InfluxDB server, once you have upgraded you local Chrome, it solved

![chrome error of InfluxDB](https://libs.websoft9.com/Websoft9/DocsPicture/zh/influxdb/influxdb-chromeerror-websoft9.png)
