# 5주차

## 오늘 배운 내용

- Docker와 컨테이너의 개념
- 가상 머신(VM)과 컨테이너의 차이
- Docker 이미지와 컨테이너의 차이
- Docker 이미지 다운로드 및 관리
- Docker 컨테이너 생성 및 실행
- 컨테이너 상태 및 로그 확인
- 포트 매핑과 환경 변수 설정
- 컨테이너 내부 접속
- 컨테이너 정지, 재시작 및 삭제
- GitHub Issue → Branch → Pull Request → Merge 협업 과정

## 새로 배운 명령어

```bash
docker --version
docker pull
docker images
docker run
docker ps
docker ps -a
docker logs
docker logs -f
docker stop
docker start
docker restart
docker rm
docker rmi
docker exec
```

## 주요 Docker 옵션

- `-d`: 백그라운드 실행
- `-it`: 대화형 터미널 실행
- `--rm`: 컨테이너 종료 시 자동 삭제
- `-p`: 포트 연결
- `--name`: 컨테이너 이름 지정
- `-v`: 볼륨 또는 디렉터리 연결
- `-w`: 작업 디렉터리 지정
- `-e`: 환경 변수 설정
