* webhook 오류.. ( 외부에서 local 접근을 못해서 )

# 도커 이미지 이미지 빌드

- -t 옵션 : 태그이름
- -f 옵션 : 원래 현재 경로 Dockerfile 을 찾아서 빌드하는데 이 옵션으로 다른파일 지정가능
- ex) docker build -t custom-jenkins:lts -f JenkinsCustomDockerfile .

* CustomJenkins 만들때 docker in docker 명령어참고 - https://blog.opendocs.co.kr/?p=704

---

#### docker compose 설치 ( 최신버전 ) // latest 자리에 버전 입력하면 해당 버전 설치

sudo curl
-L [https://github.com/docker/compose/releases/**latest**/download/docker-compose-$](https://github.com/docker/compose/releases/latest/download/docker-compose-$)(
uname -s)-$(uname -m) -o /usr/local/bin/docker-compose

* 예시 docker compose 설치버전 : v2.6.0
  sudo curl
  -L [https://github.com/docker/compose/releases/](https://github.com/docker/compose/releases/latest/download/docker-compose-$)
  v2.6.0[/download/docker-compose-$](https://github.com/docker/compose/releases/latest/download/docker-compose-$)(uname
  -s)-$(uname -m) -o /usr/local/bin/docker-compose
