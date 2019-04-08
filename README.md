# Jenkins CI/CD metrics exporter

Exports metrics from a jenkins instance in prometheus format.
Currently, this setup uses telegraf and influxdb instead of prometheus.

The exported data is queried in Grafana to get an overview of your CI/CD metrics in a dashboard.
Inspired by Lovoo's jenkins_exporter setup (https://github.com/lovoo/jenkins_exporter)

## Usage
```
$ docker-compose up #run jenkins, jenkins_exporter, telegraf, influxdb and grafana.
```




