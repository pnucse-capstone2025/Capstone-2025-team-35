### 1. 프로젝트 소개

이 프로젝트는 졸업과제를 수행하는 학생들에게 README 작성의 가이드라인을 제공하기 위해 제작되었습니다.

### 2. 팀소개

Tony Stark, ironman@marvel.com, 개발총괄

Peter Benjamin Parker, spiderman@marvel.com, 알고리즘 설계

Stephen Vincent Strange, doctorstrange@marvel.com, 백앤드 개발

Robert Bruce Banner, hulk@marvel.com, 프론트엔드 개발

### 3. 시스템 구성도

부산대학교 일반대학원 정보융합공학과는 컴퓨터공학전공, AI전공, 의생명융합전공이 있습니다.

![정보융합공학과 이미지](https://user-images.githubusercontent.com/100384365/192478661-5dc79a18-b076-48ef-b842-bcf65b0d8d44.jpg)

### 4. 소개 및 시연 영상

[![부산대학교 정보컴퓨터공학부 소개](http://img.youtube.com/vi/zh_gQ_lmLqE/0.jpg)](https://youtu.be/zh_gQ_lmLqE)

### 5. 설치 및 사용법/

본 프로젝트는 Ubuntu 20.04 버전에서 개발되었으며 함께 포함된 다음의 스크립트를 수행하여 
관련 패키지들의 설치와 빌드를 수행할 수 있습니다.
```
$ ./install_and_build.sh
```

#### 1. 클라이언트 실행 방법

#### 2. 백엔드 서버 실행 방법

본 프로젝트의 백엔드 서버는 Docker Compose 기반으로 실행됩니다.

1. **이미지 다운로드**

   ```bash
   docker compose pull
   ```

2. **컨테이너 실행**

   ```bash
   docker compose-up
   ```

3. **접속 정보**

   * App: [http://localhost:8080](http://localhost:8080)
   * MySQL: `localhost:3333` (`root/1234`, `storypool/1234`)
   * Redis: `localhost:6380` (password: `1234`)

⚠️ 이메일 발송, AWS S3, Firebase 기능은 `.env`에 Secret 값이 비워져 있어 제한됩니다.
DB, Redis, JWT 인증 및 기본 API는 정상 작동합니다.

#### 3. 인공지능 서버 실행 방법
