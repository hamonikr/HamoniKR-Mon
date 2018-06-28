# About

하모니카 리눅스를 서버로 사용하는 경우 시스템 모니터링을 쉽게 할 수 있도록 제공합니다.

쉬운 모니터링을 위하여 docker 기반의 서비스를 제공하므로, docker-compose 를 사용할 수 있는 준비가 먼저 필요합니다.

docker-compose 설치문서 : https://docs.docker.com/compose/install/

```
$ sudo apt install docker.io
$ sudo curl -L https://github.com/docker/compose/releases/download/1.21.2/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
```

# How to

이 저장소를 클론한 후에 아래의 명령을 실행하면 서비스가 구동됩니다.

```
$ docker-compose up -d
```

서비스 구동 후 아래의 주소에서 확인하세요 :

- <http://localhost:8083>  influxdb admin page
- <http://localhost:3000>  grafana web page (login with admin/admin)


grafana 로그인 후 Datasource 를 생성합니다. (influxdb dbname : collectd)

마지막으로 대시보드 ID 6696 을 임포트합니다. 


이 프로젝트와 관련하여 이슈는 상단의 이슈 탭을 이용해 주세요.
