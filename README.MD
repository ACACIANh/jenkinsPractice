* webhook 오류.. ( 외부에서 local 접근을 못해서 )

# 도커 이미지 이미지 빌드

- -t 옵션 : 태그이름
- -f 옵션 : 원래 현재 경로 Dockerfile 을 찾아서 빌드하는데 이 옵션으로 다른파일 지정가능
- ex) docker build -t custom-jenkins:lts -f JenkinsCustomDockerfile .

* CustomJenkins 만들때 docker in docker 명령어참고 - https://blog.opendocs.co.kr/?p=704