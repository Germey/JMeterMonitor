# JMeterMonitor

JMeter 测试、发送到 Influxdb、Grafana 可视化展示。

![](https://qiniu.cuiqingcai.com/2020-03-07-200213.png)

本项目为 JMeter Docker 镜像。

## 使用

拉取镜像：

```shell script
docker pull germey/jmeter
```

当前项目文件夹下新建 jmx 文件夹，存放 jmx 文件，启动：

```
docker-compose up
```

jmx 文件配置好 BackendListener，并设置好 Influxdb，直接运行即可。

## Kubernetes 部署

见 [./deployment.yml]。
