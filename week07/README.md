# 7주차

## 오늘 배운 내용

- Docker Compose 개념 및 사용법
- `compose.yaml` 파일 작성
- Web과 Redis 컨테이너 연결
- Docker Volume을 이용한 데이터 유지
- Docker 네트워크 및 컨테이너 간 통신
- `.env` 환경 변수 설정
- Healthcheck를 이용한 상태 확인
- Nginx 리버스 프록시 및 로드 밸런싱
- Scale-out을 이용한 컨테이너 확장
- Docker Compose Watch

## 새로 배운 명령어

```bash
docker compose up -d
docker compose up -d --build
docker compose down
docker compose down -v
docker compose ps
docker compose logs web
docker compose logs -f web
docker compose restart web
docker compose exec web sh
docker volume ls
docker volume inspect guestbook_redis-data
docker compose config
docker compose config --quiet
docker compose up -d --scale web=3
docker compose up --watch
docker compose watch --no-up
```

## 실습에서 사용한 명령어

```bash
cd ~/devops/guestbook
nano compose.yaml
nano nginx.conf
echo "REDIS_PASSWORD=devops1234" > .env
echo "REDIS_PASSWORD=비밀번호" > .env.example
echo ".env" >> ~/devops/.gitignore
docker compose config
docker compose up -d --build --scale web=3
docker compose ps
```
