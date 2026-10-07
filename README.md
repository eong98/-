# 장우원 | Backend Developer

> **Java · Spring Boot · JPA** 백엔드와 **Python 기반 AI(LLM · Vision)** 를 함께 다루는 개발자입니다.
> 웹에이전시에서 3년간 결제 · ERP · SOAP 연동과 서버 운영까지 직접 수행했고,
> 그 경험 위에 새로운 스택을 얹어 **AI를 서비스의 기능으로 설계하는 백엔드**로 확장하고 있습니다.
>
> 4인 AI 팀 프로젝트에서 **PL(팀장)** 으로 아키텍처와 DB 스키마를 설계했고,
> 직접 기획 · 개발 · 배포해 **실제 운영 중인 서비스(유형숲)** 도 있습니다.

📧 dndnjs6918@naver.com ・ 📱 010-9699-6918 ・ 📍 서울 관악구

---

## 📌 한눈에 보기

| 구분 | 프로젝트 | 핵심 기술 | 역할 |
|---|---|---|---|
| **AI 팀 프로젝트** | [알리미오](#-ai-팀-프로젝트--알리미오allimio--무인매장-cctv-실시간-ai-관제-시스템) — 무인매장 CCTV 실시간 AI 관제 | Spring Boot · FastAPI · YOLOv5 · Jetson · LangGraph · RAG | **PL(팀장)** · 설계 총괄 · 엣지 AI 단독 |
| **운영 중인 개인 서비스** | [유형숲](#-운영-중인-개인-서비스--유형숲-foresttypecokr) — 유형 · 궁합 · 퀴즈 테스트 플랫폼 | Spring Boot 3.5 · React 19 · Oracle · Nginx · Docker · GitHub Actions | **1인 기획 · 개발 · 배포 · 운영** |
| **개인 프로젝트** | [CLIMB:ON](#-개인-프로젝트--climbon--클라이밍-암장-검색--커뮤니티--스토어) — 클라이밍 암장 검색 · 커뮤니티 · 스토어 | Spring Boot · React · FastAPI · LangChain · JWT · 토스페이먼츠 | 1인 개발 (3-티어 전체) |
| **실무 — 커머스** | [SEKMALL](#-sekmall--b2b-쇼핑몰-구축) (B2B) / [더푸짐](#-더푸짐--b2c-쇼핑몰-구축) (B2C) | PHP · MySQL · 이카운트 ERP · 카카오 알림톡 | 메인 단독 |
| **실무 — 교육** | [스펙트럼KU](#-스펙트럼ku--교육-플랫폼--국내외-결제) / [명지전문대 KBO 야구심판](#-명지전문대-kbo-야구심판-양성과정--교육-플랫폼) | PHP · 이니시스 · PayPal | 메인 |
| **실무 — 대규모 회원** | [한국심리학회](#-한국심리학회--회원--회비--결제-시스템) (회원 5~6만) | PHP · MySQL · 결제 API | 서브 |
| **실무 — 외부 연동** | [티케이엘리베이터 IGAD](#-티케이엘리베이터코리아-igad--soap-기반-cad-연동) | PHP 8.3 · SOAP | 담당 |
| **운영** | [유지보수 150여 개사 / 300여 개 도메인](#-유지보수-담당-사이트) | Linux · Apache · PHP 5.x~8.3 | 담당 |

> ⚠️ 실무 프로젝트는 **고객사 자산이라 소스를 공개할 수 없어**, 담당 업무와 설계 의도 중심으로 정리했습니다.
> 유형숲은 운영 중인 서비스라 저장소를 비공개로 두고 있으며, 팀 프로젝트와 CLIMB:ON은 저장소 링크에서 코드를 확인할 수 있습니다.

---

## 🛠️ 기술 스택

### 현재 주력 — Backend + AI

| 구분 | 내용 |
|---|---|
| **Backend** | Java 17 · 21, Spring Boot 3.5, Spring Data JPA, Spring Security, JWT, Redis, Oracle, FastAPI |
| **Frontend** | React 19, TypeScript, Vite, Zustand, Axios |
| **AI / LLM** | Python, OpenAI API, Ollama, LangChain, LangGraph, RAG(ChromaDB), Prompt Engineering |
| **Vision / Edge AI** | YOLOv5, OpenCV, PyTorch, NVIDIA Jetson Nano, 객체 추적기 직접 구현 |
| **모델 운영** | H200 GPU 서버에 모델 직접 설치 · 설정 후 서빙, LLM 제공자 전환 구조(Ollama ↔ OpenAI) |
| **DevOps** | Docker Compose, Nginx(HTTPS), GitHub Actions(CI/CD), 가비아 클라우드(VPC · 서버 · 스토리지) |
| **설계 · 리딩** | 요구사항 정의, ERD 설계, 도메인 분리, 팀 역할 분담, Agile 기반 일정 관리 |

### 실무 기반 — 웹 서비스 개발 · 운영 3년

| 구분 | 내용 |
|---|---|
| **Backend** | PHP 5.x ~ 8.3, MySQL, REST API, SOAP |
| **Frontend** | JavaScript, jQuery, AJAX, HTML5, CSS3 |
| **Server** | Linux, Apache, SSL 인증서, 서버 운영 · 장애 대응 (20여 대) |
| **결제** | 이니시스, 토스페이, PayPal |
| **ERP** | 이카운트 ERP, SAP ERP |
| **인증 / 알림 / 통계** | 네이버 · 카카오 로그인, 카카오 알림톡, SMS, Google Analytics Data API |

---

## 🤖 AI 팀 프로젝트 — 알리미오(allimio) : 무인매장 CCTV 실시간 AI 관제 시스템

> **역할: PL(팀장) · 아키텍처 및 DB 설계 총괄 · 매장/CCTV 관제 도메인 · 엣지 AI 단독 개발**
> 4인 팀 · 2026

무인 매장의 CCTV 영상을 AI가 실시간 분석해 **폭행 · 기물파손 · 쓰러짐(응급) · 무단침입 · 장시간체류 · 화재**
6종의 이상 상황을 감지하고, 관리자에게 즉시 알리는 관제 서비스입니다.

### 저장소

| 저장소 | 구성 | 참여 |
|---|---|---|
| [team2_react_v1](https://github.com/eong98/team2_react_v1) | 프론트엔드 (React 19 · TypeScript · Vite · Zustand) | 4명 |
| [team2_jpa_v1](https://github.com/eong98/team2_jpa_v1) | 비즈니스 백엔드 (Spring Boot · JPA · Oracle · JWT · Redis) | 4명 |
| [team2_fastapi_v1](https://github.com/eong98/team2_fastapi_v1) | AI 서버 (FastAPI · LangChain · LangGraph · ChromaDB) | 4명 |
| [team2_jetson](https://github.com/eong98/team2_jetson) | 엣지 디바이스 추론 (Jetson Nano · YOLOv5) | **단독 개발** |

---

### 👤 PL(팀장) — 설계 총괄 및 팀 리딩

프로젝트 기획부터 아키텍처 확정, 팀원 역할 분담, 기술 지원까지 팀 리딩 전반을 담당했습니다.

**1. 서비스 기획 및 주제 선정**
- 무인점포 절도 신고 건수 추이(2021년 3,514건 → 2025년 11,015건, 경찰청 집계), 한국소비자원 실태조사, 실제 사건 사례를 조사해 **문제 정의와 서비스 필요성을 근거 기반으로 정리**
- 세콤 · 에스원 등 기존 물리보안 서비스와 **기능 · 요금 구조를 비교 분석**하여, "기존 CCTV만으로 별도 장비 없이 상시 AI 판단" 이라는 서비스 차별점과 **CCTV 대수 구간별 구독제** 과금 모델을 설계

**2. 전체 아키텍처 설계**
- 서비스를 **프론트엔드 / 비즈니스 백엔드 / AI 백엔드 / 엣지 디바이스** 4계층으로 분리하고 계층 간 통신 방식(REST API · WebSocket)을 정의
- 비즈니스 로직(Spring Boot)과 AI 추론(FastAPI)을 **별도 서버로 분리** — AI 연산 부하가 서비스 응답에 영향을 주지 않도록 하고, 모델 교체 시 비즈니스 코드를 수정하지 않도록 구성
- 저장소를 계층별로 4개로 나누어, 팀원이 서로의 빌드에 영향을 주지 않고 병렬 개발할 수 있는 구조 확립

**3. 통합 DB 스키마 설계 (전 도메인 ERD 작성)**
- 팀원 각자가 테이블을 따로 만들면 개발 중간에 스키마가 충돌한다고 판단해, **개발 착수 전 전 도메인 테이블을 하나의 스키마로 통합 설계**
- `SHOP` · `MEMBER` · `CCTV` · `CCTV_ISSUE` · `CCTV_VISITOR` · `SHOP_ORDER` · `SHOP_PRODUCT` · `NOTIFICATION` 등 전체 테이블과 관계를 ERD로 확정한 뒤 개발 시작
- **메뉴–페이지–DB 매핑표**와 **테이블 정의서**를 문서로 작성해 팀원 전원이 같은 기준으로 개발하도록 함
- 결과적으로 개발 도중 스키마 변경으로 인한 재작업 없이 통합 단계를 진행

**4. 팀 역할 분담 및 기술 지원**

| 팀원 | 담당 도메인 |
|---|---|
| **장우원 (PL)** | 매장 · CCTV 등록/관리, CCTV 실시간 관제, CCTV 이슈 · 방문객, 이상행동 유형코드, 매장 캘린더, 관리자/매장 메뉴 관리, 점주 대시보드 통계, Jetson 워커, CCTV 이슈 AI 검토 |
| 고찬영 | 회원가입 · 정보수정, SMS/메일 인증, 로그인(쿠키 JWT + Redis), 로그인 이력, 아이디/비밀번호 찾기, 고객의 소리 |
| 김승연 | 공지사항 · 1:1 문의(FAQ) 게시판, 첨부파일 관리, 챗봇 상담 및 대화 로그, 구독권 · 결제 내역 |
| 이은혜 | SMS 이미지 생성, SMS · 메일 발송/이력, 웹메일함 · 번역, AI 도면 생성, 만족도 조사 |

- 도메인별로 **기능 · 담당 테이블 · 페이지 범위를 문서로 확정**한 뒤 분담하여, 업무 경계에서 생기는 누락을 사전에 차단
- 팀원들이 처음 다루는 **Spring Boot · JPA 연관관계 매핑, REST API 설계, Git 브랜치 전략** 등에 대해 수시로 기술 지원 진행
- Agile 기반으로 일정을 관리하고 통합과 배포까지 담당

---

### 🎥 AI 파이프라인 설계 — 엣지 + 서버 2단계 판단 구조

**해결할 문제** — 모든 CCTV 영상을 서버로 보내 분석하면 네트워크 비용과 GPU 부하가 매장 수에 비례해 증가합니다.
반대로 엣지 디바이스에서만 판단하면 Jetson Nano의 연산 성능상 정확도가 떨어집니다.

**설계한 구조** — 판단 난이도에 따라 처리 위치를 나눴습니다.

```
[ CCTV ] ─RTSP/USB─> [ Jetson Nano ]  ──명확한 이벤트──>  [ Spring Boot ]  ──WebSocket──> [ 관제 대시보드 ]
                     YOLOv5 + 추적기                       CCTV_ISSUE 저장               (React)
                        track_id 부여                            ▲
                            │                                    │
                            └──애매한 이벤트(프레임 이미지)──> [ FastAPI + H200 ] ──최종 확정──┘
                                                               AI 재검토
```

| 단계 | 처리 위치 | 내용 |
|---|---|---|
| **① 탐지 · 추적** | Jetson Nano | YOLOv5로 사람을 탐지하고, **직접 구현한 추적기**로 `track_id` 를 부여해 입장 · 퇴장을 구분 |
| **② 1차 판단 (확정)** | Jetson Nano | 입장/퇴장(`CCTV_VISITOR`), 영업시간 외 무단침입, 장시간체류처럼 **규칙으로 확정 가능한 이벤트는 엣지에서 유형코드까지 확정**해 서버로 전송 → 영상 전송량 · 서버 부하 대폭 절감 |
| **③ 2차 판단 (재확인)** | H200 GPU 서버 | 쓰러짐 · 폭행 후보는 **해당 프레임 이미지만** 서버로 전송, AI가 실제 화면을 보고 최종 확정 → 오탐 저감 |
| **④ 저장 · 알림** | Spring Boot | 확정된 이벤트를 `CCTV_ISSUE` 에 저장하고 **WebSocket** 으로 관리자에게 실시간 알림 |

> 💡 전체 영상을 서버로 보내지 않고 **"확정 가능한 건 엣지에서, 애매한 것만 이미지로 서버에"** 로 나눈 것이 이 설계의 핵심입니다.

**모델 선정 — 왜 YOLOv5 인가**

Jetson Nano는 연산 성능과 메모리가 제한적이라, 모델 크기가 곧 실시간 처리 가능 여부를 결정합니다.
상위 버전 대비 **YOLOv5(s 모델)가 더 가볍고 Jetson 환경에서의 레퍼런스와 배포 자료가 풍부**했으며,
이 프로젝트에서 필요한 것은 세밀한 분류가 아니라 **사람 탐지와 추적** 이었기 때문에
YOLOv5로도 목표 정확도를 충분히 확보할 수 있다고 판단해 채택했습니다.
정밀 판정이 필요한 쓰러짐 · 폭행은 어차피 서버 단 2차 판정으로 넘기는 구조이므로,
엣지 모델은 **가볍고 안정적으로 계속 도는 것**이 더 중요하다고 보았습니다.

**추적기를 직접 구현한 이유**

같은 이유로 추적기도 외부 라이브러리 대신 **IOU 매칭 + 속도 예측 + 짧은 미탐지 허용** 만 갖춘 가벼운 추적기를 직접 작성했습니다.
무인 매장은 동시에 화면에 잡히는 사람 수가 적어, 무거운 추적 알고리즘보다 Jetson에서 프레임을 놓치지 않는 쪽이 판정 정확도에 더 중요했습니다.

### 🛠️ 직접 구현한 부분

**엣지 AI (단독 개발)**
- **YOLOv5s** 기반 사람 탐지, 직접 구현한 추적기로 다중 객체 추적 및 `track_id` 관리
- **NVIDIA Jetson Nano** 환경 세팅, OpenCV 기반 영상 처리
- 폭행 · 쓰러짐 · 무단침입 · 장시간체류는 추적 결과 기반 규칙으로, 기물파손 · 화재는 장면 기반 규칙으로 판정
- 방문객 입장/퇴장 집계, 감지 결과를 AI 서버 API로 전송

**AI 서버 · 모델 서빙**
- **H200 GPU 서버**에 모델을 직접 설치 · 설정하고 서빙 환경 구성
- **FastAPI** 로 이슈 접수 API 구성, CCTV 이슈를 AI가 다시 검토하는 **AI 검토(Agent)** 기능 개발

**관제 도메인 (백엔드 + 프론트)**
- 매장 · CCTV 등록/관리, CCTV 이슈 · 방문객 목록, 이상행동 유형코드 관리
- 매장 캘린더(FullCalendar), 관리자/매장 메뉴 관리(드래그앤드롭 정렬, 사이드바를 DB 메뉴로 동적 구성)
- **점주 대시보드** — 일별 · 시간대별 방문객, 일별 이슈, 유형별 이슈 비율 차트.
  회원번호를 요청 파라미터가 아닌 쿠키 JWT에서 추출해 **다른 매장 데이터 조회(IDOR)를 차단**
- 관제 대시보드 UI — 정상(그린) · 주의(앰버) · 위험(레드) 3단계 상태 체계, 데스크톱/모바일 반응형

### 기술 스택
`Spring Boot` `Spring Data JPA` `Oracle` `JWT` `Redis` `React 19` `TypeScript` `Vite` `Zustand` `FastAPI` `Python`
`YOLOv5` `OpenCV` `PyTorch` `Jetson Nano` `Ollama` `LangChain` `LangGraph` `ChromaDB` `WebSocket` `Docker`

---

## 🌳 운영 중인 개인 서비스 — 유형숲 (foresttype.co.kr)

> **[foresttype.co.kr](https://foresttype.co.kr) ・ 1인 기획 · 개발 · 배포 · 운영 ・ 2026 ・ 서비스 중**
> 저장소는 운영 중인 서비스라 비공개입니다.

유형 · 궁합 · 퀴즈 테스트를 1분 안에 하고 친구와 결과를 비교하는 테스트 플랫폼입니다.
"수익이 나는 서비스를 직접 만들어 운영해 본다"를 목표로 도메인 구매부터 배포, 검색 등록, 홍보까지 혼자 진행했습니다.

### 구조

```
[ 브라우저 ] → Nginx(443, HTTPS) → Spring Boot(jar 1개) → JPA → Oracle
                                     └ React 빌드 결과를 static에 포함해 함께 배포
```

`Spring Boot 3.5` `Java 17` `Spring Data JPA` `Oracle` `React 19` `TypeScript` `Nginx` `Docker Compose` `GitHub Actions`

### 핵심 설계 — "테스트 = 데이터"

테스트를 추가할 때마다 코드를 짜면 운영 비용이 테스트 수에 비례해 늘어납니다.
그래서 **테스트 하나를 JSON 정의 파일 하나로 표현**하고, 서버는 채점 방식 5가지만 알도록 설계했습니다.

| 채점 타입 | 방식 |
|---|---|
| `AXIS` | 축별 점수 합의 부호 조합으로 결과 결정 (궁합 옵션 지원) |
| `TALLY` | 선택지가 결과에 표를 주고 최다 득표 결과 선택 (가중치 지원) |
| `SCORE` | 점수 합계를 구간으로 나눠 결과 결정 |
| `TRIVIA` | 정답형 퀴즈. 제한 시간, 문제 은행 무작위 출제 옵션 |
| `BALANCE` | 결과 없이 문항별 투표 비율 표시 |

- **재배포 없는 콘텐츠 추가** — 관리자 화면에 JSON을 붙여넣고 검사 후 저장하면 바로 반영
- **저장 전 검증** — 도달할 수 없는 결과, 점수 구간의 빈틈 같은 정의 오류를 검증기가 저장 단계에서 차단
- **서버 재채점** — 점수표와 정답은 API로 내려보내지 않고, 제출된 답을 서버에서 다시 채점
- **Java ↔ TypeScript 채점 로직 교차 검증** — 같은 규칙이 서버와 프론트 두 곳에 있어, 검증 도구로 7,200건을 대조해 결과 차이 0건 확인

### 직접 구현한 기능

- **콘텐츠** — 테스트 30여 종(연애 · 심리 · 취미 · 직장 · 퀴즈 등), 읽을거리 20여 편, 결과별 상세 설명과 관련 테스트 추천
- **참여 · 공유** — 궁합 보기, 오늘의 퀴즈(연속 참여 기록), 점수 도전장, 친구 비교방, 카카오톡 공유, 결과별 OG 이미지와 인스타 스토리용 이미지를 서버에서 생성
- **관리자** — 테스트 편집 · 숨김, 배너 관리, 방문 통계 대시보드(퍼널 시각화)
- **통계 직접 수집** — 쿠키 없이 일별 해시로 방문을 집계하고 IP는 저장하지 않는 방식으로 구현
- **보안** — IP별 요청 제한, CSP 등 보안 헤더, CSRF 방어, 로그인 실패 잠금, 관리자 세션은 HttpOnly 쿠키 + PBKDF2
- **SEO** — robots · sitemap, 검색 엔진 등록, 초기 HTML에 정적 콘텐츠를 서버에서 렌더링

### 배포 · 운영

- **CI/CD** — 기능 브랜치 push → GitHub Actions 테스트 → main 병합 → 서버 배포 스크립트 자동 실행
- **운영 대비** — 백업 스크립트와 서버 이전 절차 문서(환경 변수 · Nginx 설정 · Oracle Data Pump) 작성
- **수익화 · 홍보** — 제휴 링크 적용, 광고 심사 대응(콘텐츠 보강 · 정책 페이지 정비), 인스타그램 릴스 제작 자동화(Python 영상 생성 스크립트)

> 💡 실무에서 150여 개 사이트를 유지보수하며 배운 "운영 단계에서 비용이 되는 구조"를 처음부터 피하려고 한 프로젝트입니다.
> 콘텐츠 추가에 개발이 필요 없게 만든 것, 배포와 백업을 자동화한 것이 그 결과입니다.

---

## 🧗 개인 프로젝트 — CLIMB:ON : 클라이밍 암장 검색 · 커뮤니티 · 스토어

> **1인 개발 ・ Spring Boot + React + FastAPI 3-티어 전체 ・ 2026**

클라이밍 암장을 난이도 · 지역 · 시설로 검색하고, 커뮤니티와 장비 스토어, AI 추천까지 제공하는 플랫폼입니다.
팀 프로젝트에서 익힌 구조를 **혼자서 처음부터 끝까지** 다시 만들어 보며 인증 · 결제 · AI 연동을 직접 설계했습니다.

### 저장소

| 저장소 | 구성 |
|---|---|
| [climb_jpa_v1](https://github.com/eong98/climb_jpa_v1) | 백엔드 (Spring Boot 3.5 · Java 21 · JPA · Oracle · Spring Security + JWT) |
| [climb_react_v1](https://github.com/eong98/climb_react_v1) | 프론트엔드 (React 19 · TypeScript · Vite · Zustand) |
| [climb_fastapi_v1](https://github.com/eong98/climb_fastapi_v1) | AI 서버 (FastAPI · LangChain · Ollama / OpenAI) |

### 구조

```
React ──REST/JWT──▶ Spring Boot ──JDBC──▶ Oracle (테이블 20개)
                        │  ▲
                        ▼  │  서버 대 서버
                     FastAPI : LLM · LangChain
```

**React는 AI 서버를 직접 호출하지 않고 항상 Spring을 거칩니다.**
- 인증 · 권한 검사를 Spring Security 한 곳에서만 처리
- AI에 넘길 데이터(리뷰, 등반일지)를 DB에서 꺼내는 주체를 Spring으로 통일
- AI 서버가 내려가도 Spring이 대체 응답을 만들어 화면이 깨지지 않음

### 핵심 설계

**1. 난이도 정규화** — 암장마다 V등급 · YDS · French · 색상 난이도를 제각각 써서 "내 수준에 맞는 암장"을 검색할 수 없는 문제를,
네 가지 체계를 **0~100 점수 하나로 환산**해 범위 검색이 가능하도록 해결했습니다.
표시값(문자)과 정렬값(숫자)을 분리 저장하고, 저장값은 항상 서버가 계산합니다.

**2. LLM 역할 분리와 장애 격리**
- 통계 계산은 Python 코드가, **해석과 코칭 문장만 LLM이** 담당 → 숫자를 지어내는 문제 방지
- 모든 AI 기능에 **규칙 기반 대체 로직**을 두어 LLM이 없어도 정상 응답
- LLM 제공자(Ollama ↔ OpenAI)를 환경 변수 하나로 전환

**3. 인증** — 액세스 토큰 + 리프레시 토큰, 재발급 시 기존 토큰을 폐기하는 회전 방식(RTR).
프론트는 axios 인터셉터로 401 발생 시 자동 재발급 후 원래 요청을 재시도합니다.

**4. 데이터 설계**
- 암장 검색은 `EXISTS` 서브쿼리 사용 (JOIN 시 중복 행으로 페이징 건수가 어긋나는 문제 방지)
- 평점 · 리뷰 수는 집계 컬럼으로 반정규화하고 리뷰 변경 시 재집계
- 주문 시점의 상품명 · 가격을 주문 상세에 복사 저장(스냅샷)해, 이후 상품이 바뀌어도 주문 내역이 유지

### 주요 기능

- **암장 검색** — 난이도 범위, 지역, 유형, 시설, 영업 중 필터 / 상세(난이도 구성, 영업시간, 리뷰, AI 리뷰 요약)
- **AI** — 자연어 검색(문장을 검색 조건으로 구조화), Q&A 챗봇, 리뷰 요약 · 감성 분석, 등반일지 실력 분석 리포트, 암장 · 장비 추천
- **커뮤니티** — 게시판 5종, 댓글/대댓글, 좋아요, 첨부
- **스토어** — 상품 · 후기, 장바구니, 주문/취소(재고 연동), **토스페이먼츠 결제 승인(테스트 모드)** — 금액 검증과 중복 승인 방지 처리
- **마이페이지** — 등반일지, 월별 추이 · 난이도별 완등 분포 그래프
- **관리자** — 암장 · 회원 · 게시글 · 상품 · 주문 · 공지 관리

`Spring Boot 3.5` `Java 21` `Spring Security` `JWT` `JPA` `Oracle` `React 19` `TypeScript` `FastAPI` `LangChain` `Ollama` `OpenAI API` `토스페이먼츠`

---

## 💼 실무 프로젝트 (피아트SID, 2022.08 ~ 2025.07)

웹에이전시에서 **고객사 웹 서비스 신규 구축 20여 건**과 **누적 150여 개 사이트 유지보수**를 병행했습니다.
아래는 대표 6건이며, 대부분 **현재까지 실제 서비스로 운영 중인 사이트**입니다.

### 🛒 SEKMALL — B2B 쇼핑몰 구축
**[sekmall.com](https://sekmall.com) ・ 메인 담당(단독) ・ 상용 서비스**

- 관리자(DBMS) 페이지 · 사용자 페이지 전반 개발
- 상품 관리, 거래처별 할인 구간, 쿠폰, 게시판 구현
- **이카운트 ERP 연동** — 주문 · 재고 · 정산 데이터 동기화
- B2B 특성상 거래처마다 단가와 할인 정책이 달라, 조건 분기로 처리하지 않고 정책 데이터 기반 구조로 분리하여 신규 거래처 추가 시 코드 수정 없이 대응하도록 설계

`PHP` `MySQL` `jQuery` `AJAX` `이카운트 ERP`

---

### 🛍️ 더푸짐 — B2C 쇼핑몰 구축
**deopujim.com *(호스팅 종료)* ・ 메인 담당(단독)**

- 관리자 · 사용자 페이지, 상품 및 할인 관리, 게시판 개발
- **카카오 · 네이버 간편 로그인** 연동
- **카카오 알림톡** 연동 — 주문 · 배송 상태 변경 시 자동 발송, 상태 이력 기준 처리로 중복 발송 방지

`PHP` `MySQL` `카카오/네이버 로그인` `카카오 알림톡`

---

### 🧠 한국심리학회 — 회원 · 회비 · 결제 시스템
**[koreanpsychology.or.kr](https://koreanpsychology.or.kr) ・ 서브 담당 ・ 상용 서비스**

- 모학회 + 분과학회 통합 **회원 5~6만 명** 규모
- 회원 등급 체계, 연회비 · 가입비 정산, 결제 시스템 개발
- 학술행사 지원 · 신청 관리 기능 개발
- 분과별로 회비 정책이 달라 등급 · 분과 · 회비를 분리 설계하여 정책 변경에 대응

`PHP` `MySQL` `결제 API`

---

### ⚾ 명지전문대 KBO 야구심판 양성과정 — 교육 플랫폼
**[baseball.mjc.ac.kr](https://baseball.mjc.ac.kr) ・ 메인 담당 ・ 상용 서비스**

- 수강생 회원 가입 및 관리
- 교육 과정 개설 · 신청 기능, 기수 · 정원 관리
- 게시판, 수료 자격증 발급 기능 개발

`PHP` `MySQL`

---

### 🎓 스펙트럼KU — 교육 플랫폼 + 국내외 결제
**[spectrumku.com](https://spectrumku.com) ・ 메인 담당 ・ 상용 서비스**

- 회원 관리, 강의 개설 및 수강 신청 기능 개발
- **이니시스 + PayPal API 연동 구축** (국내 / 해외 결제 이원화)
- 자격증 발급 및 출력 기능 개발
- PG사별 응답 포맷과 취소 · 환불 플로우가 달라, 결제 로직을 공통 인터페이스로 추상화해 PG 추가 시 확장 가능하도록 구성

`PHP` `MySQL` `이니시스` `PayPal API`

---

### 🏢 티케이엘리베이터코리아 IGAD — SOAP 기반 CAD 연동
**igad-dev.tkek.co.kr ・ 담당**

**상황** — PHP 5.x → 8.3 마이그레이션 작업 중 SOAP 통신 오류가 다수 발생

**행동** — 서버 · 자사 코드 · 외부 통신 구간으로 원인 범위를 나눠 확인한 결과,
자사 코드가 아닌 외부 CAD 업체 측 통신 규격 문제로 판단.
추정에서 멈추지 않고 업체와 회의를 진행해 규격을 맞추는 방향으로 합의

**결과** — 마이그레이션 완료 및 연동 정상화.
원인 범위를 먼저 좁히는 접근과 외부 업체와의 기술 커뮤니케이션을 경험

`PHP 8.3` `SOAP` `외부 시스템 연동`

---

## 🎓 교육

**솔데스크 — 가비아 g클라우드 기반 그룹웨어 개발자 양성과정** (2026.04 ~ 2026.10)

1. JAVA 프로그래밍 — OOP, 클래스/메서드, 파일 I/O 및 CSV 처리
2. DBMS 설계 및 최적화 — SQL, 트랜잭션 관리, 데이터 분석 쿼리
3. Spring Full-Stack 웹 개발 — Spring Boot, DI/애노테이션, RESTful API 설계
4. Python 데이터 분석 & 자동화 — 모듈/패키지, Network/DBMS 연동, 분석 모듈 활용
5. 프롬프트 엔지니어링과 ChatGPT 통합 — STT, GPT 스트리밍 응답, LLM 활용
6. g클라우드 실무 — VPC, 서버 설정, Docker 및 컨테이너 관리, 클라우드 DB/스토리지
7. g클라우드 Advanced — 서버 모니터링, 보안 설정, 자동화 스크립트, CDN
8. Team 프로젝트 — Agile 설계, GitHub Actions CI/CD, Spring Boot·JPA·OpenAI 연동, Docker 배포

**그린컴퓨터아카데미 — UI/UX 웹디자인 · 웹퍼블리셔 과정** (2021.09 ~ 2022.02)

---

## 📜 자격증

| 취득일 | 자격증 | 발급기관 |
|---|---|---|
| 2026.09 | 정보처리산업기사 | 한국산업인력공단 |
| 2026.09 | SQL 개발자 (SQLD) | 한국데이터산업진흥원 |
| 2022.03 | 웹디자인개발기능사 | 한국산업인력공단 |
| 2019.09 | GTQ 포토샵 1급 (국가공인) | 한국생산성본부 |
| 2016.09 | 전자기능사 | 한국산업인력공단 |

**학력** — 학점은행제 정보처리학과 재학 중 (2026.08 ~) · 서울전자고등학교 전자과 졸업

---

## 🔧 유지보수 담당 사이트

3년간 **누적 150여 개사 / 300여 개 도메인**의 웹 서비스 운영과 유지보수를 담당했습니다.
서버 환경 · PHP 버전 · 개발사가 모두 달라, 낯선 코드베이스를 빠르게 파악하고 대응하는 경험을 쌓았습니다.

**담당 업무**
- Linux / Apache 웹 서버 20여 대 운영, SSL 인증서 설치 및 갱신
- 서비스 장애 발생 시 로그 · 환경 분석을 통한 원인 파악 및 조치
- PHP 5.x → 8.3 버전 마이그레이션 다수 수행 (Deprecated 함수 대응, 호환성 검증)
- 고객사 요구사항 분석을 통한 기능 개선 및 재개발

### 주요 고객사

| 분류 | 고객사 |
|---|---|
| **대학 · 교육** | 고려대학교(경영대학 · 공과대학 · 의과대학 · 보건과학대학 외), 경희대학교(경영대학원 · 글로벌미래교육원 · AI비즈니스MBA 외), 서울대학교(SSBT · SSRT 외), 명지전문대학, 경기대학교, 안양대학교, 한국원자력연구원(RCARO) |
| **대기업 · 제조** | HD현대오일뱅크, 현대케미칼, 현대쉘베이스오일, 현대오일터미널, 현대코스모, 현대리바트, 슈나이더일렉트릭코리아, 티케이엘리베이터코리아, 롯데베르살리스 엘라스토머스, 아남전자, 덕신하우징 |
| **협회 · 학회** | 한국심리학회, 한국석유화학협회, 한국제지연합회, 한국화학섬유협회, 한국광고주협회, 한국경영과학회, 국제경영원, 항공우주정책연구원, 공군사관학교총동창회 |
| **의료** | 고려대학교의료원(부정맥), 삼성서울병원 순환기내과, 서울아산병원 부정맥센터, 강동미즈여성병원, 사과나무치과병원, 온세메디칼 |
| **건설 · ERP** | 신동아건설, 대지건설, 보성건설, 금강인프라건설, 정안건설, 선풍토건, 일해토건, 신흥건설 (다수 ERP 시스템 포함) |
| **쇼핑몰 · 커머스** | 에쓰오일 포인트몰 · 파트너몰, GS파트너몰, SEKMALL, 더푸짐, 한의바이오 |
| **공공** | 강북구청(생활지리정보 · 여성정보), 경주시장애인체육회, 월드비전 경기남지부 |

<details>
<summary><b>📋 전체 유지보수 사이트 목록 펼쳐 보기 (원본)</b></summary>

```
현대오일뱅크(주) OBP,oilbankbiz.net
경희대학교 AI 비즈니스MBA,aimba.khu.ac.kr
현대오일뱅크(주) OBP,oilbankbiz.com
피아트SID(주),fiart.net
(주)피아트코리아,fiart.co.kr
(주)한방케어,hanbangcarecar.co.kr
(주)에스에이치글로벌,www.shglobal.kr
현대오일뱅크 엑스티어,
영도한의원,ydh.kr
공군인터넷전우회(로카피스),rokafis.or.kr
피아트SID(주),ezgw.fiart.kr
피아트SID(주),ezhrms.fiart.kr
신동아건설(주),sdaconst.co.kr
신동아건설(주),familie.co.kr
티엔에스슈퍼데크,tnssuperdeck.com
정원한의원,stepdiet.net
(주)에스엔유티씨엔티,sekmall.com
(주)대지건설,daejienc.co.kr
(주)온세메디칼,onsemedical.co.kr
(주)온세메디칼,medtrics.co.kr
(주)온세메디칼,heart.pe.kr
한방당뇨네트워크,dangclinic.com
(주)제이원모터스,hondacarsj-one.co.kr
(주)디텍,incdt.net
(주)한백산,siru.co.kr
(주)한백산,sirusan.co.kr
(주)한백산,jtrading.co.kr
(주)한백산,hbsan.com
(주)에이치티엠,like.htmco.kr/ijis
지에스건설(주),gongse.co.kr
삼구건설(주),39c.co.kr
(주)에이치티엠,ho.htmco.kr
노메스한의원,nomes.seeok.co.kr
(주)하이큐시스템,hpsvc.kr
강동미즈여성병원,gmh.or.kr
(주)한국티이아이,teikorea.com
(사)국제경영원,m.imi.or.kr
랩케어진단검사의학과의원,labcare.kr
(사)한국심리학회,koreanpsychology.kr
경희대학교 글로벌미래교육원,kaca.khu.ac.kr
(주)한국기독교정보,christland.net
에쓰오일포인트몰(한백산),soil.hbsan.com
한중한의원,hjclinic.co.kr
삼삼엔지니어링(주),samsam.biz
공군전우회,airforce.ne.kr
고려대학교의료원 (부정맥),ep.kumc.or.kr
(주)씨엘뱅크,pluscar.clb.co.kr
다앤미,55diet.com
(주)일해토건,ilhae21.com
(주)일해토건,erp.ilhae21.com
(주)돌엔돌,doln.net
애니콤정보통신(주),anycomm.net
고려콜렉션,korea-col.co.kr
김주성한의원,kjsclinic.co.kr
(주)텔레컨스,telecons.co.kr
신진메딕스(주),diakey.com
(주)한국기독교정보,christinfo.co.kr
서경정보통신,kt-megapass.net
선주토건(주),sunjoo21.co.kr
(주)크레온유니티,icreon.co.kr
(주)지투디앤씨,g2dnc.co.kr
지엔지주식회사,gng-steel.co.kr
(주)텔레컨스,mapzin.co.kr
아산병원부정맥센터,amc-heartrhythm.com
(주)한산기연,hansaneng.co.kr
사단법인 항공우주정책연구원,kapi.or.kr
(주)한백산,shop.oilbankbiz.com
(주)커뮤니케이션소리,lucebr.co.kr
(주)그로넷테크놀러지,giftzone.oilbankcard.com
(주)이알씨라인,ercline.com
(사)국제경영원,imi.or.kr
올웨이즈앤애프앤비(주),drstuarts.co.kr
한상훈한의원,dr-han.co.kr
사하한의원,sahaclinic.co.kr
씨티에스엔지니어링(주),ctseng.com
(주)벨루션네트웍스,bellution.com
보성건설(주),bosung21.com
가나철거공사,gn7904.com
(사)한국가스연맹,kgu.or.kr
평강한의원,daligra.com
(주)이본종합건설,pajuhuton.com
SAMKOO Vina,samkoo.fiart.kr
평강한의원,55clinic.com
(주)유니디아,unidia.co.kr
인스유아이,dainmd.com
강아지농장,skpet.co.kr
(주)씨엘뱅크,clb.co.kr
(주)유엔터스,uenters.com
(사)국제경영원,newhrd.fiart.kr
금강인프라건설(주),kgcon.kr
(주)한국이엔아이인터네셔날,messeworld.co.kr
경희대학교 AI 비즈니스MBA,smartlab.khu.ac.kr
(주)하이큐시스템,hiqsys.co.kr
강북구청(생활지리정보),wgis.gangbuk.seoul.kr
평강한의원,seeok.co.kr
미인나라,mi-in.co.kr
(주)모노커뮤니케이션즈,mono.co.kr
(주)이본종합건설,pajuhuton.co.kr
피아트SID(주),easyerp.kr
(주)컴투프리테크,comtopritech.co.kr
평강한의원,daligra.co.kr
(주)이슈텔레콤,is-telecom.co.kr
사하한의원,antipain.net
(주)온세메디칼,clamed.co.kr
선풍토건(주),sunpoong.co.kr
(주)하니에이엠씨,dogdr.co.kr
(주)하니에이엠씨,animaltrap.co.kr
현대네트웍스(주),hdnetworks.co.kr
고려대학교의료원(흉통),koreaheart.co.kr
(사)대한민국공군발전협회,arokaf.co.kr
생명교회,lifegiving.or.kr
(주)더블유오케이,romadalgujitour.com
현대쉘베이스오일(주),hsbaseoil.co.kr
경희대학교 경영대학원,golf.khu.ac.kr
공군사관학교총동창회,kafaaa.or.kr
씨엠알기술연구원(주),cmr.or.kr
에쓰오일포인트몰(한백산),mall.s-oilbonus.com
한국김치플랜트산업 주식회사,kimchiplant.co.kr
아남전자(주),aname.co.kr
아남전자(주),anamglobal.com
(주)케이티엘솔루션,kt-service.co.kr
(주)포유,famille-gangdong.co.kr
동광리어유한회사,dklear.com
현대코스모㈜ 서울지점,hyundaicosmo.com
(주)고우넷,itsm.gownet.com
정원한의원,stepdiet.co.kr
디피알파트너(주),dpr.or.kr
동광기연(주),dktec.co.kr
(주)유니디아,summit-tech.co.kr
(주)비와이넷플러스,
(주)텔레컨스,rubie.co.kr
한국석유화학협회,kpia.or.kr
에쓰오일포인트몰(한백산),intranet.hbsan.com
피아트SID(주),fiart.kr
(주)양음스탁119,st119.com
(주)미디어비엠코리아,gogobm.co.kr
(주)미디어비엠코리아,gogobm.com
(주)미디어비엠코리아,gogobm.net
(주)미디어비엠코리아,gogobm.kr
눈치코치,seeok.co.kr
(주)대지건설,daejienc.com
법무법인 온누리,onnurilaw.com
사하한의원,energyclinic.kr
미인나라,miinsoo.com
피지피기술(주),pgptech.co.kr
영천레포츠(주),www.exposkyfly.co.kr
(주)세계로물산,plows.co.kr
(주)한백산,intranet.hbsan.com
해피텔레콤,happy-tel.com
현대오일뱅크(주) 고객자문단,ob.oilbank.co.kr
혜성씨앤씨(주),hscnci.com
눈치코치,s-ok.co.kr
대명리프트,dmrental.co.kr
월드비전 경기남지부,wvgyeonggi.or.kr
강북구청(여성정보),women.gangbuk.go.kr
(주)하이큐시스템,hpzone.co.kr
고대 심장혈관 연구소,cwri.co.kr
(주)한백산,elohas.co.kr
(주)커뮤니케이션소리,botanicparktower.co.kr
(주)인휴,inhuedeco.co.kr
지에이시(GAC) 닥터아토앤비,atopyskin114.com
(주)트라이텍코리아,triteckorea.co.kr
아남전자(주),anamworldwide.com
현대오일뱅크(주) 고객자문단,advice.oilbank.co.kr
현대케미칼주식회사,www.hyundaichemical.co.kr
노블레스싱글텔,nbtel.co.kr
유벨라,ubella.co.kr
유벨라,ubella.kr
리코이엔씨주식회사,byuksong.co.kr
(유)우양자원,wy-recycling.kr
올웨이즈앤애프앤비(주),drstuartshop.co.kr
피아트SID(주),sm.fiart.kr
주식회사 이던인터내셔날,eathun.co.kr
신동아건설(주),m.sdacon.co.kr
(주)지앤티글로벌,gntglobal.com
(주)지투디앤씨,g2dnc.com
(주)한백산,shop.hbsan.com
현대오일뱅크 엑스티어,
(주)에스엔유티씨엔티,eocrmall.com
(주)포유,viewsky.co.kr
주식회사 다우시스,polynaru.com
현대오일뱅크(주) OBP,oilbank.co.kr
경기대학교,kgumie.com
(주)커뮤니케이션소리,healing-state.co.kr
(주)커뮤니케이션소리,metrocity2.co.kr
한국김치플랜트산업 주식회사,kimchimachine.co.kr
동광기연(주),dktec.co.kr
한국RC협의회,krcc.or.kr
한국RC협의회,hichem.or.kr
군자출판사(주),koonja.co.kr
글로북스,gbooks.kr
(주)쉬스케미칼컨설팅,sheschem.com
(주)쉬스케미칼컨설팅,sheschem.co.kr
(주)쉬스케미칼컨설팅,sheschem.kr
커뮤니케이션즈 리치(주),botanicparktower.co.kr
디에스인터내셔널(주),dsint.net
(재)에이치디현대일퍼센트나눔재단,hdhyundainanum.or.kr
(재)에이치디현대일퍼센트나눔재단,honor.hdhyundainanum.or.kr
미인나라,m.mi-in.co.kr
(주)한의바이오 쇼핑몰,dr-yakcho.co.kr
신동아건설(주),familieapt.co.kr
웰리스다이어트(쑥나린),ssuknarin.com
(주)에스에이치글로벌,www.shglobal.co.kr
탐나는아동복탑랜드상가운영회,seoultopland.co.kr
고려대학교 지속가능원,sustainability.korea.ac.kr
달빛소리 영농조합법인,mv01.co.kr
명지전문대학 평생교육원,edu.mjc.ac.kr
(주)지투디앤씨,goldenfeetcnd.co.kr
(주)한방케어,10care.co.kr
(주)인터크레존,daelim-acrotel.co.kr
현대오일터미널(주),www.oilterminal.co.kr
(주)디자인벽지,designwallpaper.co.kr
보임서비스(주),voimservice.com
공군인터넷전우회(로카피스),kafi.net
(주)티에스비즈텍,tsbiz.net
현대오일뱅크 엑스티어,
현대쉘베이스오일(주),hsbaseoil.com
(주)세계로물산,isaacfood.co.kr
(주)커뮤니케이션소리,wg3.co.kr
(주)커뮤니케이션소리,biz.hausd.co.kr
(주)덕신하우징,duckshin.com
(사)한국의료행정실무협회,simsa.kr
(주)쉬스케미칼컨설팅,sheschem.com
경희대학교 경영대학원,asp.khu.ac.kr
올웨이즈앤애프앤비(주),drstuartshop.co.kr
해피텔레콤,hms.happy-tel.com
한국화학소재기술연구조합,chemtra.or.kr
(사)국제경영원,m.newhrd.com
리코이엔씨주식회사,reeco.co.kr
한국당뇨협회,dangnyo.or.kr
경희대학교 경영대학원,wmba.khu.ac.kr
아남전자(주),m.anamglobal.com
(주)도담이앤씨종합건축사무소,dodam.fiart.kr
당큐(한방당뇨),dangclinic.co.kr
에이치디현대오일뱅크(주) 서울지점,shop.oilbankbiz.com
폰타나리조트,fontana-resort.co.kr
폰타나리조트,fontana-resort.kr
(주)한방케어,carecar.co.kr
(주)에이치티엠,han.dreamit.kr
아남전자(주),m.aname.co.kr
신동아건설(주),m.familie.co.kr
(주)덕신하우징,duckshinvina.com
(주)덕신하우징(전자입찰),duckshin.com
경희대학교 총동문회(경영대학원),kyungheemba.com
금천수병원,
(주)디에스엘,globaldsl.co.kr
(주)커뮤니케이션소리,botanicparktower2.net
경희대학교 경영대학원,khmbachina.khu.ac.kr
(주)커뮤니케이션소리,familie-sp.co.kr/maintain
경희대학교 경영대학원,mil.khu.ac.kr
사과나무치과병원,appledental.kr/m
사과나무치과병원,appledental.kr
사과나무치과병원,miraeassetshopping.com
사과나무치과병원,hanwhashopping.com
(주)에스에이치글로벌,www.shglobal.kr
(주)에스에이치글로벌,shglobal.co.kr
경희대학교 경영대학원,ceo.khu.ac.kr
(주)휴먼아이티,
모새골,heart.pe.kr/_fiart
(주)휴먼아이티,
경희대학교 경영대학원,khmba.khu.ac.kr
현대오일뱅크 엑스티어,
(사)국제경영원,newhrd.com
경희대학교 국제대학원,gsp.khu.ac.kr
(재)한국지식재산관리재단,kipf.or.kr
이웃사랑임대사랑 사회적협동조합,이웃사랑임대사랑.kr
주식회사 다우시스,dowsys.co.kr
주식회사 다우시스,dowsys.net
청풍인삼,
온넷시스템,dainmd.com
(주)디케씨코퍼레이션,dkcor.com
현대오일뱅크 엑스티어,
(주)커뮤니케이션소리,ryumatower.co.kr
(주)커뮤니케이션소리,mabukutovill.co.kr
(주)에이치티엠,dtsys.kr
슈나이더일렉트릭코리아(주),schneider-electric.co.kr
슈나이더일렉트릭코리아(주),legacy.schneider-electric.co.kr/m/
한국화학섬유협회,kcfa.or.kr
주식회사 제이앤피하우징랜드,
(주)드림텔레시스,dtsys.kr
피아트SID(주),gw.fiart.kr
슈나이더일렉트릭코리아(주),schneider2
슈나이더일렉트릭코리아(주),schneider4
슈나이더일렉트릭코리아(주),eschneider
신길5동지역주택조합,singil5.com
슈나이더일렉트릭코리아(주),service-frame-kr.se.com
선풍토건(주),erp.sunpoong.co.kr
(유)우양자원,erp.wy-recycling.kr
금강인프라건설(주),erp.kgcon.kr
한국제지연합회,paper.or.kr
(주)커뮤니케이션소리,botanicparktower3.com
JPC오토모티브,jwpre.com
(주)한성리소스산업,erp.hs-recycling.com
(사)국제경영원,imi.or.kr
(사)국제경영원,imilec.or.kr
서울대역편백숲1차지역주택조합설립추진위원회,healing-state.co.kr
서울대역편백숲1차지역주택조합설립추진위원회,healingstate.co.kr
(주)에너넷,iener.net
삼성서울병원 순환기내과,arrhythmia.co.kr
한국RC협의회,aprcc2019.com
귀천 주식회사,1668-0000.co.kr
제이와이커스텀(주),jycustom.com
(주)에이치티엠,internet-korea.kr
(주)에이치티엠,lucky7.co
한국건드릴(주),gundrill.co.kr
군자출판사(주),smarteduk.co.kr
군자출판사(주),smarteduk.com
경희대학교 글로벌미래교육원,cce.khu.ac.kr
(재)한경협중소기업협력센터,www.fkilsc.or.kr
경희대학교 일본로컬문화연구회,japanlocal.khu.ac.kr
경희대학교 글로벌미래교육원,ccea.khu.ac.kr
경희대학교 글로벌미래교육원,ccek.khu.ac.kr
(주)한의바이오,hanibio.kr
한의부항학회(한의바이오),k-act.or.kr
한국화학산업연합회,kocic.or.kr
한국제지연합회,ilovepaper.org
경희대학교 글로벌미래교육원,practicaldance.khu.ac.kr
(주)한의바이오 쇼핑몰,hanibio.co.kr
(주)한의바이오 쇼핑몰,dr-yakcho.com
(주)한성로지스,hs-logis.co.kr
(사)국제경영원,forum.imi.or.kr
(주)온세메디칼,arrhythmia.co.kr
눈치코치,m.seeok.co.kr
경희대학교 글로벌미래교육원,klc.khu.ac.kr
아이디비넷 주식회사,yesas.co.kr
제이와이커스텀(주),jymap.co.kr
영도한의원,china.ydh.kr
경희대학교 글로벌미래교육원,air.khu.ac.kr
(사)한국의료행정실무협회,cyber.simsa.kr
(주)온세메디칼,insui.co.kr
(주)온세메디칼,ercline.com
(주)온세메디칼,dainmd.com
(주)온세메디칼,snamd.com
(주)에스에이치글로벌,dktec.co.kr
한국석유화학협회,ilovechem.kr
귀천 주식회사,1668-0000.com
귀천 주식회사,1668-0000.net
㈜제이엔커뮤니케이션즈,ilovechem.kr
(주)온세메디칼,saeronnetworks.com
㈜제이엔커뮤니케이션즈,ilovechem.co.kr
한국석유화학협회,ilovechem.co.kr
(주)디앤에프,decknfuture.com
경희대학교 글로벌미래교육원,beauty.khu.ac.kr
(사)한국광고주협회,kaa.or.kr
경희대학교 글로벌미래교육원,mamp.khu.ac.kr
(주)대지건설,erp.daejienc.com
(사)국제경영원,online.imi.or.kr
(사)국제경영원,newhrd.net
고려대학교 경영대학,biz.korea.ac.kr
동화예건(주),dw.inhuedeco.co.kr
역북지역주택조합,yukbuk.co.kr
재단법인 무봉,mubong.org
고려대학교 경영대학,biz.korea.ac.kr/bk21four/main/main
한국원자력연구원(RCARO),e-campus.rcaro.org/
하니동물병원,animaltrap.co.kr
하니동물병원,dogdr.co.kr
주식회사 비앤드브이,multiflooring.com
신산SS토건(주),sinsan.co.kr
경희대학교 경영대학원,emba.khu.ac.kr
(주)신흥건설,shin-heung.com
(주)신흥건설,shdnc.co.kr
새론네트웍스,saeronnetworks.com
클라메드,clamed.co.kr
고려대학교 아세아문제연구원,asiaticresearch.org
고려대학교 반도체공학과,se.korea.ac.kr
피아트SID(주),message.fiart.kr
에쓰오일파트너몰(한백산),s-partner.s-oil.com
(주)네트인,netin.kr
GS파트너몰(한백산),with-partnermall.com
한신자원산업,h-shin.kr
경희대학교 빅데이터응용학과,bigdata21.khu.ac.kr
(사)국제경영원,member.imi.or.kr
(주)버킷인터내셔날,bucketint.co.kr
고려대학교 건축학과 교우회,kua1964.com
고려대학교 경영대학,kubsrankings.korea.ac.kr
고려대학교 경영대학,www.s3-asiamba.com
고려대학교 VLSISP Lab.,vlsisp.korea.ac.kr
고려대학교산학협력단,kukistschool.korea.ac.kr
(주)시루산,siru.co.kr
경희대학교 경영대학원,wamp.khu.ac.kr
고려대학교 전기전자공학부,ee.korea.ac.kr
경주시장애인체육회,gyeongjusad.or.kr
고려대학교 차세대통신학과,ce.korea.ac.kr
유한메카트로닉스(주),mall.yu-han.co.kr
(주)이솝,ysop.co.kr
(주)이솝,mall.ysop.co.kr
삼주공인노무사사무소,sjoffice.co.kr
고려대학교 대학원혁신본부,graduate.korea.ac.kr
대한제지(주),www.daehanpaper.com
군자출판사(주),www.medicalpictures.co.kr
군자출판사(주),www.mediteriumart.com
군자출판사(주),www.mediteriumart.co.kr
(주)텔레컨스,mcon-service.azurewebsites.net
(주)스펙트럼케이유,spectrumku.com
(사)한국심리학회,koreanpsychology.or.kr
(주)파블로항공,www.pabloair.com
성우안보전략연구원,www.starflag.or.kr
경희대학교 (AMP),ceo.khu.ac.kr
(주)세문,semun.co.kr
고려대학교 기업산학연협력센터,uric.korea.ac.kr
(주)하나일렉트릭,www.hnec.co.kr
고려대학교 건축학과 교우회,kua1964.kr
안양대학교 평생교육원,ay.fiart.kr
(사)국제경영원,newhrd.net
(주)에스에이치글로벌,hrms.shglobal.kr
고려대학교 경영대학,biz.korea.ac.kr/cdc/main/main.html
서울대학교 SSBT (차세대이차전지),ssbt.snu.ac.kr
성준전기(주),sungjoon.co.kr
(사)한국의료행정실무협회,simsa.fiart.kr
(주)인휴,ih.inhuedeco.co.kr
(주)하나일렉트릭,mall.hnec.co.kr
한국과학기술출판협회,kstpa.or.kr
고려대학교 KU-KIST융합대학원,kukistschool.korea.ac.kr
한국출판인산악회,kpmclub.com
더푸짐주식회사,deopujim.com
(사)성무안보연구소,www.srins.re.kr
아티크스튜디오 주식회사,artiquestudio.co.kr
롯데베르살리스 엘라스토머스㈜,lvelastomers.com
경희대학교 빅데이터응용학과,bk21bigdata.khu.ac.kr
명지전문대학 조기취업형계약학과,early.mjc.ac.kr
고려대학교 인권·성평등센터,humanrights.korea.ac.kr
성준전기(주),mall.sungjoon.co.kr
명지전문대학 평생교육원,sv80.fiart.kr
한국과학기술출판협회,mall.kstpa.or.kr
한국소비자광고심리학회,kscap.co.kr
티케이엘리베이터코리아(주)-IGAD,igad-dev.tkek.co.kr
티케이엘리베이터코리아(주)-IGAD,rigad-dev.tkek.co.kr
(주)에이치티엠,internet-korea.kr/m/main/main.html
에이치디현대오일뱅크(주) 서울지점,oilbank.fiart.net
고려대학교 지속가능원,kusr.korea.ac.kr
다스코리아(주),daskorea.co.kr
디에스인터내셔널(주),duckshinint.com
명지전문대학 MRCC,mrcc.mjc.ac.kr
명지전문대학 MRCC,mrcc.fiart.net
고려대학교 공과대학,eng.korea.ac.kr
(주)쉬스케미칼컨설팅,loa.sheschem.com
명지전문대학 평생교육원,baseball.mjc.ac.kr
고려대학교의료원 (부정맥),korea-heartrhythm.com
다스코리아(주),110.45.213.175
경희대학교 총동문회(경영대학원),
공군인터넷전우회(로카피스),kafi.fiart.net
고려대학교 미디어대학,mediacom.korea.ac.kr
서울시광역심리지원센터,koreanpsychology.or.kr/mind/introduction.html
고려대학교 경영대학,esg.korea.ac.kr
고려대학교 경영대학,www.aicg.org
현대네트웍스(주),flucare.co.kr
(주)에스엔유티씨엔티,snutcnt.com/
(주)엘제이하이테크,lj-hitech.co.kr
(주)현대리바트,shop.oilbankbiz.com
고려대학교 지속가능원,kusso.korea.ac.kr
(재)한국문화예술진흥재단,koracf.or.kr
(주)에스엔유티씨엔티,sekmall.co.kr
고려대학교 기계공학부,me.korea.ac.kr
서울대학교 Advanced Energy Materials Lab,energylab.snu.ac.kr
서울대학교 SSRT,ssrt.snu.ac.kr
(주)덕신하우징,dukshinepc.com
고려대학교의료원,korea-heartrhythm.com
(주)비포시스템,bfsystem.kr
티케이엘리베이터코리아(주)-TIS,customer.tkek.co.kr
(주)덕신하우징(전자입찰),dukshinepc.com
(사)한국경영과학회,komsri.kr
(사)한국경영과학회,komsri.co.kr
(사)한국경영과학회,komsri.or.kr
(주)비포시스템,bfsystem.kr/BIMS
서울대학교 Advanced Energy Materials Lab,
군자출판사(주),smarteduk.fiart.net
경희대학교 경영연구원,mri.khu.ac.kr
주식회사 비앤드브이,bnv.fiart.net
고려대학교 건축학과,archi.korea.ac.kr
(사)로카피스생활체육회,rokafis.com
(주)비포시스템,bfsystem.kr/KFCC/login.htm
(주)비포시스템,be4.co.kr
(재)에이치디현대희망재단,hdhyundaihope.org
(주)모노커뮤니케이션즈,
고려대학교 보건과학대학,chs.korea.ac.kr
고려대학교 보건과학대학,bmeng.korea.ac.kr
고려대학교 보건과학대학,bsm.korea.ac.kr
고려대학교 보건과학대학,hes.korea.ac.kr
고려대학교 보건과학대학,hpm.korea.ac.kr
더푸짐주식회사,inifood.co.kr
(주)비포시스템,mgit.co.kr
고려대학교 건축학과,
명지전문대학 평생교육원,early.mjc.ac.kr
명지전문대학 야구심판양성과정,baseball.mjc.ac.kr
주식회사 비앤드브이,floorcovering.co.kr
서울시광역심리지원센터,mt.koreanpsychology.or.kr
(주)정안건설,jaenc.kr
고려대학교 공학대학원,enggra.korea.ac.kr
고려대학교 공학대학원,ceo.korea.ac.kr
고려대학교 의과대학,kumstp.korea.ac.kr
고려대학교 MRC 마이오카인 융합연구센터,myokinemrc.korea.ac.kr
경희대학교 경영연구원,mri.fiart.net
명지전문대학 조기취업형계약학과,early.fiart.net
고려대학교 미디어대학,mediacom.fiart.net
(주)덕신이피씨,duckshin.com
주식회사 비앤드브이,flooringcatalogue.com
(사)한국심리학회 재난심리위원회,dp.koreanpsychology.or.kr
(주)덕신하우징,dukshinhousing.com
고려대학교 의과대학,kumstp.fiart.net
(주)에이엔케이이노베이션,ankinnovation.com
(주)정안건설,erp.jaenc.kr
(주)덕신이피씨,duckshin.com
(주)덕신이피씨,duckshinepc.com
(주)덕신이피씨,dukshinepc.com
티케이엘리베이터코리아(주)-TIS,igad-dev.tkek.co.kr
(사)한국의료행정실무협회,simsa.fiart.net
```

</details>
