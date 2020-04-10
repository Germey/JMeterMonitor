# JMeterMonitor

JMeter 测试、发送到 Influxdb 或 Prometheus、Grafana 可视化展示。

![](https://qiniu.cuiqingcai.com/2020-03-07-200213.png)

本项目为 JMeter Docker 镜像。

注：Prometheus 需要依赖 [https://github.com/johrstrom/jmeter-prometheus-plugin](https://github.com/johrstrom/jmeter-prometheus-plugin)，镜像已经内置。

## 使用

拉取镜像：

```shell script
docker pull germey/jmeter
```

当前项目文件夹下新建 jmx 文件夹，用于存放 jmx 文件。JMeter 中配置好 BackendListener，并设置好 Influxdb，测试成功后，将配置保存到 jmx 文件夹。

启动：

```
docker-compose up
```

会永久运行测试并发送测试数据到 Influxdb，Grafana 可视化展示即可。

## Kubernetes 部署

见 [kubernetes/deployment.yml](kubernetes/deployment.yml)。

## 参考来源

[https://github.com/justb4/docker-jmeter](https://github.com/justb4/docker-jmeter)。
