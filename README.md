### 1. 프로젝트 배경
#### 1.1. 국내외 시장 현황 및 문제점
 최근 아이들을 대상으로 한 AI 기반 이야기 생성 서비스가 다수 개발되어 있다. 본 연구에서는 기존 서비스들의 특징과 한계를 분석하여 개발 방향성을 도출하고자 한다.
1) 모두의 동화
주요 기능: 사용자가 직접 이야기의 내용을 작성하고, 표지를 꾸미며, 완성된 이야기를 다른 사용자와 공유할 수 있는 플랫폼 제공한다.
장점: 사용자 주도적 창작 경험 제공, 공동체 공유를 통한 성취감 부여
단점: 이야기 생성이 전적으로 사용자에게 의존하므로, 부적절하거나 편향된 내용이 포함될 가능성이 있다. AI 기반 검증 기능이 없어 관리가 어렵다는 문제가 제기됨.
2) Storybook AI
주요 기능: 생성형 AI를 기반으로 그림 동화를 생성하며, 문장 단위로 사용자가 내용을 확인(confirm)하고 피드백을 제공할 수 있음.
장점: 사용자가 원하는 내용을 적극적으로 반영할 수 있어 맞춤형 이야기 생성 가능. 즉각적 피드백을 통해 만족도 향상.
단점: 주 이용자가 아동이라는 특성으로 인해, 이야기가 길어지면 집중력이 떨어지고 흥미를 쉽게 잃음. 문장 단위 확인 과정이 오히려 사용자의 몰입을 방해할 수 있음.
3) Storybookly
주요 기능: 생성형 AI 기반의 그림 동화 웹 서비스로, 부드러운 색감과 친숙한 그림체 제공.
장점: 시각적 친밀감이 높아 아동의 흥미 유발에 효과적임.
단점: 배경음악이나 사운드 효과가 제공되지 않아 몰입 경험이 제한됨. 사용자 경험 향상을 위한 멀티모달 요소 부족.
 종합적으로 살펴보았을 때, 기존 서비스들은 각기 차별화된 장점을 가지고 있으나, 아동 사용자 특성과 AI 기반 생성 과정에서 발생할 수 있는 문제점을 충분히 보완하지 못하고 있다. 특히 사용자 주도형 서비스에서는 부적절한 콘텐츠 발생 가능성이 높고, 생성 과정에서 반복 확인이 요구되는 서비스는 집중력 저하와 흥미 상실 문제를 야기한다. 또한 몰입 경험을 강화할 수 있는 멀티모달 요소(배경음악, 사운드 등)의 부재도 공통된 한계로 나타난다.

#### 1.2. 필요성과 기대효과
  일기 쓰기는 학생들이 글쓰기 능력을 기르고, 자신의 경험을 서술하며, 더 나아가 자아를 이해하고 미래의 자신에게 소중한 추억을 전달하는 데 중요한 교육적 의미를 지닌다. 그러나 일부 학생들에게 일기 작성은 지루하고 부담스러운 과제로 인식되기도 하며, 이러한 이유로 학습 효과가 저하되는 경우가 있다. 반대로 일기 쓰기를 즐기는 학생들조차도 자신이 기록한 일기를 더욱 생생하게 표현하거나, 등장인물과 사건을 확장하여 상상력을 발휘하고 싶어 하는 경우가 많다.
 
  따라서 일기를 바탕으로 그림 동화 이야기를 자동으로 생성해 주는 애플리케이션은 학생들에게 새로운 동기를 부여할 수 있다. 일기를 쓰기 힘들어하는 학생들에게는 즐겁게 글쓰기에 접근할 수 있는 계기를 제공하고, 일기를 좋아하는 학생들에게는 자신의 글을 구체화하고 확장할 수 있는 창의적 경험을 제공한다. 이러한 과정은 단순한 기록 활동을 넘어, 개인의 일상과 상상이 결합된 새로운 형태의 이야기 창작 경험으로 이어질 수 있다.

   나아가 본 연구는 단순히 동화를 생성하는 데 그치지 않고, 인공지능(AI)을 활용하는 과정에서 필요한 프롬프트(prompt) 작성 기능을 학생들이 직접 경험할 수 있도록 기능을 확장하고자 한다. 이를 통해 학생들은 AI 시대에 요구되는 핵심 역량 중 하나인 대규모 언어 모델(LLM) 활용 능력을 자연스럽게 익히고, 보다 유창하고 주도적으로 AI와 상호작용할 수 있는 능력을 기를 수 있다.

### 2. 개발 목표
#### 2.1. 목표 및 세부 내용
 본 연구의 목표는 아동이 자신의 일기를 바탕으로 그림 동화 이야기를 생성하는 과정에서, 사용자 경험, 콘텐츠 생성, 학습·심리적 효과를 종합적으로 고려한 애플리케이션을 개발하는 것이다.
 
1. 사용자 경험(UX) 향상
> 인터페이스는 직관적이고 간단하게 설계하여, 일기 작성, 촬영, 업로드 등 일련의 과정이 원활히 진행되도록 한다.
 비동기 처리와 즉각적 응답을 지원하여, 파이프라인 작업 중에도 사용자가 다른 활동을 수행할 수 있도록 한다.
 작업 완료 시 푸시 알림을 제공하여, 사용자가 진행 상태를 쉽게 확인할 수 있도록 한다.
 전체 애플리케이션은 빠른 처리 속도와 높은 반응성을 제공하여 아동의 집중력과 흥미를 유지한다.
2. 감정 기반 이야기 생성
> 사용자의 입력에서 드러나는 감정과 핵심 요소를 최대한 활용하여 이야기를 생성한다. 부적절한 내용은 필터링하되, 부정적 감정이나 특징적 요소는 적절히 반영하여 사용자 경험과 심리적 진정성을 유지한다. 사용자의 감정은 그림으로 시각화되며, 교육자와 보호자가 피드백을 제공할 수 있도록 한다.
3. 학습적·심리적 효과 강화
> 일기와 감정을 기반으로 이야기를 생성하면서, 새로운 시각과 객관적 관점을 제공한다. 이를 통해 사용자가 다양한 관점에서 상황을 이해하고, 사고력과 상상력을 확장할 수 있도록 한다. 호기심을 자극하는 요소를 적극 반영하여 학습 동기를 강화하고, 이야기 경험의 몰입도를 높인다.

#### 2.2. 기존 서비스 대비 차별성 
본 프로젝트는 오픈소스 모델을 기반으로 한 온프레미스 서버형 애플리케이션입니다. 따라서 학교나 유치원 등 교육기관은 별도의 비용 부담 없이, 전산실 등 내부 서버에 배포하여 자유롭게 사용할 수 있습니다.

기존 서비스들은 서버리스 구조 또는 자체 제작·오픈소스 모델을 활용하면서도 이용료가 발생하는 경우가 많습니다. 반면 본 프로젝트는 가벼운 모델을 활용하여 비용 부담 없이 원하는 만큼 사용할 수 있도록 설계되었습니다. 덕분에 교육기관에서도 손쉽게 도입할 수 있으며, Docker 등을 통한 편리한 배포 환경도 제공합니다.

또한 본 프로젝트는 단순한 기능 제공을 넘어, 아이들과 AI 간의 활발한 상호작용을 통해 창의력과 적응력을 키우는 데 초점을 맞추고 있습니다. AI 시대를 살아갈 아이들이 제약 없이 시도하고 경험할 수 있도록 설계된 점이 기존 서비스와의 가장 큰 차별성입니다.

#### 2.3. 사회적 가치 도입 계획 
본 프로젝트는 단순히 한 번 사용하고 끝나는 애플리케이션이 아니라, 지속적인 발전과 교육적 순환 구조를 지향합니다. 우리 학교 내의 코드코치와 같은 교육봉사 동아리, 그리고 인근 학교와의 연계를 통해 전산실에 배포·운영하고, 아이들이 직접 사용해보며 생기는 문제나 개선점을 피드백하는 체계를 마련할 예정입니다. 더 나아가, 학생들이 직접 프롬프트를 조정하거나 기능을 개선할 수 있도록 하여 참여형·창의형 프로젝트로 발전시킵니다.

또한 프로젝트 유지와 개선에 필요한 비용은 상업적 목적이 아닌, 공익적 광고를 활용해 충당할 계획입니다. 예를 들어, 애플리케이션 내 게시판 기능에 사회적 가치가 담긴 광고—공익 마케팅, 노담 캠페인, 학생 복지 관련 홍보 등—를 게재함으로써 학생들에게 도움이 되는 동시에 프로젝트의 지속성을 보장합니다.

이와 같은 구조는 단순한 도입을 넘어, 교육기관과 학생, 그리고 지역사회가 함께 만들어가는 자생적이고 지속 가능한 AI 교육 생태계를 구현한다는 점에서 의미가 있습니다.

### 3. 시스템 설계
#### 3.1. 시스템 구성도

![시스템구성도](https://github.com/pnucse-capstone2025/Capstone-2025-team-35/blob/main/src/storypool_architecture.png)

#### 3.2. 사용 기술

##### 1. 인공지능(AI) 서버

##### 모델 및 프레임워크
- **Hugging Face Hub**  
  - 모델, 데이터셋, 토크나이저 공유 플랫폼  
  - *Inference API*: 서버리스 추론 서비스 (무료 버전 토큰 제한 존재)

- **Transformers**  
  - 사전학습 트랜스포머 모델 저장/추론/재학습/미세조정 프레임워크  
  - 다양한 토크나이저 제공  

- **Sentence Transformers**  
  - 문장 임베딩 특화 프레임워크  
  - Cosine Similarity 기반 검색, 시맨틱 검색, 클러스터링 지원  

##### 번역 모델
- **Helsinki-NLP/opus-mt-ko-en**  
  - 대표적인 오픈소스 한–영 번역 모델  
  - BLEU: 41.3  

- **NHNDQ/nllb-finetuned-en2ko**  
  - NHN 다이퀘스트 영–한 번역 모델  
  - BLEU: 33.66  

##### 언어 모델
- **LLaMA (Meta AI)**  
  - 대규모 트랜스포머 기반 언어 모델 시리즈  
  - 다양한 크기 및 추론 툴 제공  

- **Ollama**  
  - 로컬 환경에서 LLaMA 계열 모델 실행 지원 플랫폼  
  - CPU 기반 실행 가능, 모델 다운로드 및 관리 지원  

- **LLaMA 3.2B**  
  - 소형 언어 모델 (3.2B 파라미터)  
  - 다양한 양자화 기법(Int4, Int8) 적용  

- **nreimers/MiniLM-L6-H384-uncased**  
  - 경량 Sentence Embedding 모델  
  - Self-supervised contrastive learning 기반  

##### 이미지 생성
- **Stable Diffusion XL (stabilityai/stable-diffusion-xl-base-1.0)**  
  - 텍스트 기반 이미지 생성 모델  
  - Base / Refiner 구조, OpenCLIP-ViT 기반 인코더 활용  

##### 비동기 처리
- **Redis Queue (RQ) + Worker 구조**  
  - 작업 등록 → 큐 → 워커 → 결과 반환  

##### Scene Parsing & Prompting
- **Scene Parsing (LLM 활용)**  
  - 이야기 데이터를 씬 단위 JSON 구조화  
  - One-shot prompt + 재시도 로직 + 누락 보정  

- **Prompt Maker**  
  - 씬별 등장인물/의상/소품/상호작용 요소 생성  
  - 일관성과 정밀도를 강화한 이미지 프롬프트 생성  

##### 2. 서버 및 백엔드

##### 프로그래밍 언어 / 프레임워크
- **Java 21**
- **Spring Boot 3.x** (REST API, 의존성 주입, 자동설정)
- **Gradle (Groovy DSL)** 빌드 도구

##### 외부 서비스 연동
- **Firebase Cloud Messaging** (실시간 푸시 알림)  
- **Gmail SMTP** (인증/알림 이메일)  
- **AWS S3** (파일 업로드/저장, Presigned URL 방식)  

##### 서버 인프라 및 운영 환경
- **AWS Route 53** (도메인/DNS 관리)  
- **Cloudflare Tunneling** (보안·네트워크 보호)  
- **Nginx** (HTTPS/SSL 리버스 프록시)  
- **Docker** (컨테이너 기반 배포/이식성 확보)  

##### 데이터베이스 및 캐시
- **MySQL** (관계형 DB, JPA/Hibernate)  
- **Redis** (캐시, 세션 관리, 인증 코드 관리, RQ 기반 Job Queue)  

##### 아키텍처 특성
- **Domain-Oriented Architecture** (도메인 중심 구조)  
- **RESTful API + Swagger (OpenAPI 3.1)** 문서화  
- **JWT 인증** (Access/Refresh 토큰, Spring Security 기반 필터 체계)  

##### 3. 클라이언트 앱

##### OCR
- **Google ML Kit for OCR**  
  - 손글씨/이미지 → 텍스트 변환  
  - Android ML Kit Vision API 활용  

##### 애플리케이션 개발
- **Unity (6000.0.44f1)**  
  - UI/UX 설계 (Canvas, Button, TextMeshPro 등)  
  - API 연동 (UnityWebRequest 비동기 호출)  
  - 배경음악 제공 (동화 분위기 기반)  
  - Animation Component 활용 시각효과 제공  

### 4. 개발 결과
#### 4.1. 전체 시스템 흐름도

![시스템흐름도](https://github.com/pnucse-capstone2025/Capstone-2025-team-35/blob/main/src/storypool_flowchart.png)

#### 4.2. 기능 설명 및 주요 기능 명세서
##### AI Pipeline 모듈 입출력 명세

##### 1. Translator
- **입력(Input):** 한국어 일기 텍스트
- **출력(Output):** 영어로 번역된 일기 텍스트


##### 2. Story Writer
- **입력(Input):** 번역된 일기 텍스트 (영어)
- **출력(Output):** 해당 내용을 기반으로 작성된 이야기 텍스트

##### 3. Scene Parser
- **입력(Input):** 이야기 텍스트
- **출력(Output):** JSON 형식의 씬 정보
```json
{
  "scene_number": "1",
  "scene_title": "",
  "characters": [],
  "time": "",
  "mood": "",
  "story": "",
  "dialogue_count": "",
  "location": ""
}
```
##### 4. Prompt Maker

- **입력(Input):** Scene Parser 결과 JSON
- **출력(Output):** 씬별 이미지 생성용 프롬프트
- 포함 내용: 주요 인물, 오브젝트, 외형 묘사, 행동 묘사, 장소 묘사

##### 5. Image Maker
- **입력(Input):** Prompt Maker에서 생성된 씬별 프롬프트
- **출력(Output):** 생성된 이미지 파일 또는 URL

##### 6. Notification
- **입력(Input):** 없음 (DB에 기록된 Story 정보를 사용)
- **출력(Output):** 웹서버 호출을 통한 알림 전송

#### 4.3. 디렉토리 구조
##### ai 서버 디렉토리 구조
```
.storypool_ai_pipeline/
│
├── apis.py
├── main.py
├── requirements.txt
│
├── api_caller/
│   ├── api_caller_interface.py
│   ├── api_caller_selector.py
│
├── emotion_classifier/
│   ├── emotion_classifier_interface.py
│   ├── emotion_classifier_manager.py
│   ├── emotion_classifier_selector.py
│
├── image_maker/
│   ├── image_maker_interface.py
│   ├── image_maker_manager.py
│   ├── image_maker_selector.py
│
├── llama_tools/
│   ├── llama_api_caller.py
│   ├── llama_helper.py
│
├── object_analyst/
│   ├── object_analyst_interface.py
│   ├── object_analyst_manager.py
│   ├── object_analyst_selector.py
│
├── ocr/
│   ├── easy_ocr.py
│   ├── ocr_interface.py
│   ├── ocr_manager.py
│   ├── ocr_selector.py
│
├── prompt_maker/
│   ├── llama_prompt_maker.py
│   ├── prompt_maker_interface.py
│   ├── prompt_maker_manager.py
│   ├── prompt_maker_selector.py
│
├── scene_parser/
│   ├── basic_scene_parser.py
│   ├── scene_parser_interface.py
│   ├── scene_parser_manager.py
│   ├── scene_parser_selector.py
│
├── story_writer/
│   ├── llama_story_writer.py
│   ├── story_writer_interface.py
│   ├── story_writer_manager.py
│   ├── story_writer_selector.py
│
└── translator/
    ├── marian_translator.py
    ├── nllb_translator.py
    ├── translator_interface.py
    ├── translator_manager.py
    ├── translator_selector.py
```

### 5. 설치 및 실행 방법
#### 5.1. 설치절차 및 실행 방법
##### ai 파이프라인 서버
##### ai 파이프라인 서버 요구사항
- Python 3.12+
- requirements.txt 참고
- diffusers==0.34.0: 딥러닝 기반 이미지 생성 및 변환 모델(예: Stable Diffusion)을 쉽게 사용할 수 있도록 돕는 라이브러리
- easyocr==1.7.2: 다양한 언어를 지원하는 간편한 OCR(문자 인식) 라이브러리
- fastapi==0.115.14: Python으로 빠르고 효율적인 REST API 서버를 쉽게 개발할 수 있는 웹 프레임워크
- httpx==0.28.1: 비동기 및 동기 HTTP 요청을 지원하는 고성능 HTTP 클라이언트 라이브러리
- numpy==2.3.1: 고성능 수치 계산을 위한 배열 및 행렬 연산 라이브러리
- Pillow==11.2.1: Python에서 이미지 처리와 조작을 위한 라이브러리 (PIL의 후속)
- pydantic==2.11.7: 데이터 유효성 검사 및 설정 관리를 위한 타입 기반 모델링 라이브러리
- pytest==8.4.1: Python 테스트 코드 작성과 실행을 도와주는 테스트 프레임워크
- sentence_transformers==4.1.0: 문장 임베딩 벡터 생성 및 문장 간 유사도 계산에 특화된 라이브러리
- torch==2.7.1: 딥러닝 모델 개발에 널리 쓰이는 PyTorch 라이브러리
- transformers==4.53.0: Hugging Face에서 제공하는 다양한 사전학습 NLP 모델 사용 라이브러리
- uvicorn==0.35.0: ASGI 기반 비동기 Python 웹서버, 주로 FastAPI와 함께 사용됨

##### 설치
프로젝트
```bash
git clone https://github.com/jiwoong5/storypool_ai_pipeline.git
cd storypool_ai_pipeline
pip install -r requirements.txt
```
llama 모델 - 3.2b - 3B  
- [llama download](https://www.llama.com/llama-downloads/)
- [ollama_download](https://ollama.com/download)
- ollama pull llama3.2:3b

##### 실행
```bash
docker compose up
```
##### 웹서버
Submodule 참고

##### 클라이언트
1. Unity 공식 사이트나 unity Hub을 통해 **Unity 6000.0.44f1**버전 다운로드
2. **git lfs**가 없다면 반드시 설치(크기가 큰 파일을 다룰 때 사용)
```bash
git lfs install
```
3. storypool-client 레포지토리를 원하는 경로에서 clone
```bash
git clone https://github.com/haenghaeng/storypool-client
```
3. Unity Hub에서 **Unity 6000.0.44f1**버전으로 **Universal 3D Core**로 임의의 프로젝트 생성
4. 프로젝트가 실행되면, **Assets - Import Package - Custom Package**를 선택 후, 다운받은 패키지를 불러옴
5. apk파일은 USB포트를 컴퓨터와 연결한 뒤 파일을 전송하여 휴대폰에 설치
6. 로컬 서버에서 테스트를 할 경우, **Assets/Scripts/Http/Global** 위치에 있는 **AppConstants.cs**을 열어 **public const string server**를 **http://localhost:8080**로 변경


### 6. 소개 자료 및 시연 영상
#### 6.1. 프로젝트 소개 자료

https://github.com/pnucse-capstone2025/Capstone-2025-team-35/blob/main/docs/03.%EB%B0%9C%ED%91%9C%EC%9E%90%EB%A3%8C/%EB%B0%9C%ED%91%9Cppt.pptx
 
#### 6.2. 시연 영상
 
https://www.youtube.com/watch?v=4BcCm-qAaCs

### 7. 팀 구성
#### 7.1. 팀원별 소개 및 역할 분담

##### 차행철
- Unity engine 기반 클라이언트 어플리케이션 제작
- UI/UX에 필요한 이미지, 애니메이션 제작
- Google ML kit OCR을 활용한 텍스트 인식
- 서버에서 제공하는 API를 기반으로 httpRequest 생성

##### 오지웅
- 동화 생성을 위한 Core AI Model 활용
- 이미지 생성을 위한 절차 설계 및 제작
- 클라이언트 어플리케이션 제작 보조

##### 최광진
- 동화 공유 플랫폼을 위한 서버 제작
- Al Model, 클라이언트 사이의 데이터 전달 설계
- DB설계 및 데이터관리
- 인증 및 보안설계
- API 설계 및 Package 구조 설계
- 인프라 설계 및 외부 서비스 연동

#### 7.2. 팀원 별 참여 후기

##### 오지웅
- 혼자라면 엄두 못낼 프로젝트를 다같이 함께해서 극복할 수 있었다.
- 신선한 주제의 프로젝트를 요즘 핫한 ai 모델들을 활용해서 완성할 수 있었다.
- docker나 github 등 협업을 위한 툴들을 활용해볼 수 있는 기회였다.
- 사용자 입력 또는 생성형 ai 기반의 응용프로젝트에서 단계별 모니터링과 타입체크, 결과물 체크 등의 중요성을 알 수 있었다.

##### 차행철
- Unity를 활용하여 기존에는 자주 사용하지 않던 UI 컴포넌트를 많이 다룰 수 있었다.
- 클라이언트와 서버 간 협업을 어떻게 진행하는 지 이번 기회에 알 수 있었다.
- Unity로 어떻게 Android에 빌드를 하고, 빌드 할 때 알아야 할 점을 배울 수 있었다.
- 협업 과정을 어떻게 조율하고, 업무 배정을 어떻게 해야 하는지 알 수 있었다.

### 8. 참고 문헌 및 출처
[1] Robin Rombach, Andreas Blattmann, Dominik Lorenz, Patrick Esser, and Björn Ommer, "High-Resolution Image Synthesis with Latent Diffusion Models," arXiv preprint arXiv:2307.01952, 2023.

[2] Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova, "BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding," arXiv preprint arXiv:1910.03771v2, 2019.

[3] Nils Reimers and Iryna Gurevych, "Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks," arXiv preprint arXiv:2108.08877, 2021.

[4] Hugo Touvron, Louis Martin, Kevin Stone, Peter Albert, Amjad Almahairi, et al., "LLaMA: Open and Efficient Foundation Language Models," arXiv preprint arXiv:2302.13971, 2023.

[5] Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, et al., "Attention is All You Need," Advances in Neural Information Processing Systems (NeurIPS), pp. 5998-6008, 2017.

[6] Banghao Chen, Yuanzhe Chen, Xue Jiang, et al., "Unleashing the Potential of Prompt Engineering in Large Language Models: A Comprehensive Review," arXiv preprint arXiv:2310.14735, 2023.

[7] The University of Western Australia, "Emotional Psychology: Understanding Emotions and Feelings," University of Western Australia, 2023. [Online]. Available: https://online.uwa.edu/news/emotional-psychology
