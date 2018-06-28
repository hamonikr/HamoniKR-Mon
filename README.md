# About

This repository shows how to use a docker compose file to setup a local collectd, influxdb, grafana stack,

You can use this repository to try collect system data, store it in influxdb and create graph chart in Grafana.


# How to

It's easy, just clone this repository and run:

```
$ docker-compose up -d
```

Then you can open:

- <http://localhost:8083>  influxdb admin page
- <http://localhost:3000>  grafana web page (login with admin/admin)

After that, import grafana dashboard ID 6696

Good luck.

