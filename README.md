# ローカルテスト用環境

手元で試したい場合に使うGrafana環境。

## 前提条件

以下の実施が必要

### grafanaユーザを作成

```
$ sudo adduser --system -uid 472 -gid 0 grafana
```

### grafanaコンテナのデータ保存先ディレクトリの作成

オーナーをgrafanaでGrafanaのデータディレクトリを作成
```
$ mkdir gf-data
$ sudo chown grafana:root gf-data
```

## 起動方法

```
$ docker-compose up -d
```

## 補足

* adminのPWは admin です
* HTTP_PROXYが必要な場合は、コメントを外して設定ください
* Prometheusなどをお試し痛い場合は [Monitoring a Linux host with Prometheus, Node Exporter, and Docker Compose | Grafana Labs](https://grafana.com/docs/grafana-cloud/quickstart/docker-compose-linux/) を参考にすると良いかも
