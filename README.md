# About

하모니카 리눅스를 서버로 사용하는 경우 시스템 모니터링을 쉽게 할 수 있도록 제공합니다.

쉬운 모니터링을 위하여 docker 기반의 서비스를 제공하므로, docker-compose 를 사용할 수 있는 준비가 먼저 필요합니다.

이미 설치되어 있다면 서비스 실행 으로 넘어가세요.

아래는 우분투 계열에서 docker, docker-compose 의 설치방법입니다.
```
$ sudo apt install docker.io
$ sudo usermod -aG docker ${USER}
$ sudo apt install docker-compose
```
## 참고
- Docker 설치문서 : https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04
- docker-compose 설치문서 : https://docs.docker.com/compose/install/



# 서비스 실행

이 저장소를 클론한 후에 아래의 명령을 실행하면 서비스가 구동됩니다.

```
$ sudo docker-compose up -d
```

서비스 구동 후 아래의 주소에서 확인하세요 :

- <http://localhost:3000>  grafana web page (login with admin/admin)




# 대시보드 설정

grafana 로그인 후 아래의 정보대로 Datasource 를 생성합니다. 
- url : http://influxdb:8086
- influxdb dbname : collectd

마지막으로 대시보드 ID 6696 을 임포트합니다. 



### Tip. 네트워크 디바이스가 eth0 이 아닌경우
ifconfig 명령어로 확인하여 사용 중인 네트워크 디바이스명을 확인하고
collected.conf 파일에서 <Plugin interface> 섹션의 interface 값을 수정하고 다시 시작하세요.



# 버그 제출 및 기타 이슈 제안
이 프로젝트와 관련하여 이슈는 상단의 이슈 탭을 이용해 주세요.
