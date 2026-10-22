# 6주차

## 오늘 배운 내용

- Dockerfile 개념 및 작성 방법
- Dockerfile 주요 명령어 (`FROM`, `WORKDIR`, `COPY`, `RUN`, `EXPOSE`, `CMD`, `ENV`)
- Docker 이미지 빌드 및 실행
- 이미지 레이어와 빌드 캐시
- Docker 이미지 태그 및 버전 관리
- Docker Hub와 GHCR 이미지 공유
- 멀티 아키텍처 이미지 빌드

## 새로 배운 명령어

```bash
docker build
docker images
docker run
docker logs
docker tag
docker push
docker pull
docker login
docker logout
docker rmi
docker image inspect
docker buildx build
```

## 실습에서 사용한 명령어

```bash
docker build -t guestbook:v1 .
docker images | grep guestbook
docker run -d -p 8081:5000 --name gb guestbook:v1
docker logs gb
docker rm -f gb

docker build -t guestbook:v1.1 .
docker build -t guestbook:v1.2 .
docker build -f Dockerfile.bad -t guestbook:bad .
docker rmi guestbook:bad

gh auth token | docker login ghcr.io -u GitHub아이디 --password-stdin
docker tag guestbook:v1 ghcr.io/아이디/guestbook:v1
docker push ghcr.io/아이디/guestbook:v1
docker pull ghcr.io/아이디/guestbook:v1

docker image inspect guestbook:v1 --format '{{.Architecture}}'
docker buildx build --platform linux/amd64,linux/arm64 -t ghcr.io/아이디/guestbook:v1 --push .
```
