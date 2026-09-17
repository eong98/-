# 장우원 | Backend Developer

> LAMP 환경에서 3년간 웹 서비스 신규 구축과 운영을 담당해 온 개발자입니다.
> 결제 · ERP · SOAP 등 외부 시스템 연동과 서버 운영까지 직접 수행했으며,
> 현재는 **Java/Spring Boot · JPA** 와 **Python 기반 LLM · AI Agent** 로 스택을 확장해
> 웹 서비스 전반을 이해하는 백엔드 개발자로 성장하고 있습니다.
>
> 최근 진행한 4인 AI 팀 프로젝트에서는 **PL(팀장)** 으로 전체 아키텍처와 DB 스키마를 설계하고,
> 팀원별 도메인 분담과 기술 지원까지 담당했습니다.

📧 dndnjs6918@naver.com ・ 📱 010-9699-6918 ・ 📍 서울 관악구

> ⚠️ 실무 프로젝트 소스는 **고객사 자산으로 공개할 수 없어**, 담당 업무와 구현 내용 중심으로 정리했습니다.
> 코드가 공개된 프로젝트는 아래 **AI 팀 프로젝트 / 개인 프로젝트** 섹션의 저장소 링크를 참고해 주세요.

---

## 🛠️ 기술 스택

### 실무 경험 (3년)

| 구분 | 내용 |
|---|---|
| **Backend** | PHP 5.x ~ 8.3, MySQL, REST API, SOAP |
| **Frontend** | JavaScript, jQuery, AJAX, HTML5, CSS3 |
| **Server** | Linux, Apache, SSL 인증서, 서버 운영 · 장애 대응 (20여 대) |
| **결제** | 이니시스, 토스페이, PayPal |
| **ERP** | 이카운트 ERP, SAP ERP |
| **인증 / 알림 / 통계** | 네이버 · 카카오 로그인, 카카오 알림톡, SMS, Google Analytics Data API |

### 교육 · 프로젝트 경험

| 구분 | 내용 |
|---|---|
| **Backend** | Java, Spring Boot, Spring Data JPA, Spring Security, Oracle, FastAPI |
| **Frontend** | React, TypeScript |
| **DevOps** | Docker, GitHub Actions (CI/CD), 가비아 g클라우드 (VPC · 서버 · 스토리지) |
| **AI / LLM** | Python, OpenAI API, LangChain, LangGraph, RAG, Vector DB, Tool Calling (AI Agent), Prompt Engineering, Streamlit |
| **Vision / Edge AI** | PyTorch, YOLOv5 · YOLOv8n, ByteTrack, OpenCV, NVIDIA Jetson Nano |
| **모델 운영** | H200 GPU 서버에 모델 직접 설치 · 설정 후 Ollama / Hugging Face 기반 서빙 (Gemma) |
| **설계 · 리딩** | 요구사항 정의, ERD 설계, 도메인 분리, 팀 역할 분담, Agile 기반 일정 관리 |

---

## 🤖 AI 팀 프로젝트 — 알리미오(allimio) : 무인매장 CCTV 실시간 AI 관제 시스템

> **역할: PL(팀장) · 아키텍처 및 DB 설계 총괄 · 매장/CCTV 관제 도메인 · 엣지 AI 단독 개발**
> 4인 팀 · 2026

무인 매장의 CCTV 영상을 AI가 실시간 분석해 **무단침입 · 쓰러짐(응급) · 폭행 · 기물파손 · 장시간체류**
5종의 이상행동을 감지하고, 관리자에게 즉시 알리는 관제 서비스입니다.

### 저장소

| 저장소 | 구성 | 참여 |
|---|---|---|
| [team2_react_v1](https://github.com/eong98/team2_react_v1) | 프론트엔드 (React · TypeScript · Vite) | 4명 |
| [team2_jpa_v1](https://github.com/eong98/team2_jpa_v1) | 비즈니스 백엔드 (Spring Boot · JPA · Oracle) | 4명 |
| [team2_fastapi_v1](https://github.com/eong98/team2_fastapi_v1) | AI 서버 (FastAPI · Python · LLM 연동) | 4명 |
| [team2_jetson](https://github.com/eong98/team2_jetson) | 엣지 디바이스 추론 (Jetson Nano · YOLO) | **단독 개발** |

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
| **장우원 (PL)** | 매장 · CCTV 등록/관리, 실시간 관제, CCTV 이슈 처리, 이상행동 유형코드 이벤트 관리 |
| 고찬영 | 회원가입 · 정보수정, SMS/메일 인증, 로그인 이력, 아이디/비밀번호 찾기, 고객의 소리 |
| 김승연 | 공지사항 · 1:1 문의(FAQ) 게시판, 첨부파일 관리, 챗봇 상담 및 대화 로그, 구독권 · 결제 내역 |
| 이은혜 | SMS 이미지 생성, SMS · 메일 발송/이력, 웹메일함 · 번역, AI 도면 생성, 만족도 조사 |

- 도메인별로 **기능 · 담당 테이블 · 페이지 범위를 문서로 확정**한 뒤 분담하여, 업무 경계에서 생기는 누락을 사전에 차단
- 팀원들이 처음 다루는 **Spring Boot · JPA 연관관계 매핑, REST API 설계, Git 브랜치 전략** 등에 대해 수시로 기술 지원 진행
- Agile 기반으로 일정을 관리하고, GitHub Actions CI/CD와 Docker 배포까지 통합 담당

---

### 🎥 AI 파이프라인 설계 — 엣지 + 서버 2단계 판단 구조

**해결할 문제** — 모든 CCTV 영상을 서버로 보내 분석하면 네트워크 비용과 GPU 부하가 매장 수에 비례해 증가합니다.
반대로 엣지 디바이스에서만 판단하면 Jetson Nano의 연산 성능상 정확도가 떨어집니다.

**설계한 구조** — 판단 난이도에 따라 처리 위치를 나눴습니다.

```
[ CCTV ] ─RTSP/USB─> [ Jetson Nano ]  ──명확한 이벤트──>  [ Spring Boot ]  ──WebSocket──> [ 관제 대시보드 ]
                      YOLO + ByteTrack                      CCTV_ISSUE 저장              (React)
                      track_id 부여                              ▲
                            │                                    │
                            └──애매한 이벤트(프레임 이미지)──> [ FastAPI + H200 ] ──최종 확정──┘
                                                              비전 모델 재판정
```

| 단계 | 처리 위치 | 내용 |
|---|---|---|
| **① 탐지 · 추적** | Jetson Nano | YOLO + **ByteTrack** 으로 사람을 탐지하고 `track_id` 를 부여해 입장 · 퇴장을 구분 |
| **② 1차 판단 (확정)** | Jetson Nano | 입장/퇴장(`CCTV_VISITOR`), 영업시간 외 무단침입, 장시간체류처럼 **규칙으로 확정 가능한 이벤트는 엣지에서 유형코드까지 확정**해 서버로 전송 → 영상 전송량 · 서버 부하 대폭 절감 |
| **③ 2차 판단 (재확인)** | H200 GPU 서버 | 쓰러짐 · 폭행 후보는 **해당 프레임 이미지만** 서버로 전송, 비전 모델이 실제 화면을 보고 최종 확정 → 오탐 저감 |
| **④ 저장 · 알림** | Spring Boot | 확정된 이벤트를 `CCTV_ISSUE` 에 저장하고 **WebSocket** 으로 관리자에게 실시간 알림 |

> 💡 전체 영상을 서버로 보내지 않고 **"확정 가능한 건 엣지에서, 애매한 것만 이미지로 서버에"** 로 나눈 것이 이 설계의 핵심입니다.

### 🛠️ 직접 구현한 부분

**엣지 AI (단독 개발)**
- **YOLOv8n / YOLOv5** 기반 사람 탐지 모델 적용, **ByteTrack** 으로 다중 객체 추적 및 `track_id` 관리
- **NVIDIA Jetson Nano** 환경 세팅 및 모델 경량화, OpenCV 기반 RTSP/USB 카메라 영상 처리
- 체류 시간 · 영업시간 · 출입 기록을 조합한 이상행동 판정 로직 구현

**모델 서빙**
- **H200 GPU 서버**에 모델을 직접 설치 · 설정하고 **Ollama / Hugging Face(Gemma)** 기반 서빙 환경 구성
- **FastAPI** 로 AI 추론 API 구성, **OpenAI API** 를 활용한 이벤트 요약 기능 연동

**관제 도메인 (백엔드 + 프론트)**
- 매장 · CCTV 등록/관리, CCTV 이슈 처리, 이상행동 유형코드 이벤트 관리, 매장 QR코드 생성 기능 개발
- 관제 대시보드 UI 구현 — 정상(그린) · 주의(앰버) · 위험(레드) 3단계 상태 체계,
  메인 CCTV + 썸네일 구조의 홈캠 스타일 화면, 데스크톱(사이드바) / 모바일(하단 탭바) 반응형 대응
- 매장별 구독권 · 구독 내역(`SHOP_PRODUCT`, `SHOP_ORDER`) 구조 설계 및 구현

### 기술 스택
`Spring Boot` `Spring Data JPA` `Oracle` `React` `TypeScript` `Vite` `Axios` `FastAPI` `Python` `oracledb`
`YOLOv8n/v5` `ByteTrack` `OpenCV` `PyTorch` `Jetson Nano` `Ollama` `LangChain` `Gemma(H200)` `OpenAI API`
`WebSocket` `REST API` `Docker` `GitHub Actions`

---

## 🧪 개인 프로젝트

| 프로젝트 | 내용 | 기술 |
|---|---|---|
| **SQL → JPA Repository 생성기** | SQL 쿼리를 입력하면 대응하는 JPA Repository 메서드를 생성. 실무에서 반복 작업을 함수화하던 습관을 LLM Tool Calling으로 확장 | Python, OpenAI API, Tool Calling, Pydantic |
| **문서 요약기** | 업로드한 문서를 벡터화해 검색 후 요약. RAG 파이프라인 구성 | LangChain, Vector DB, Streamlit |
| **Spring Boot + React CRUD** | JPA 연관관계 매핑, REST API 설계, 프론트-백엔드 분리 구조 | Spring Boot, JPA, React |
| **웹 자동화 / 크롤링** | 반복 수집 업무 자동화 후 수집 데이터 분석 | Selenium, BeautifulSoup, Pandas |

---

## 💼 실무 대표 프로젝트 (피아트SID, 2022.08 ~ 2025.07)

웹에이전시로, **고객사 웹 서비스 신규 구축 20여 건**과 **누적 150여 개 사이트 유지보수**를 병행했습니다.

### 🛒 SEKMALL — B2B 쇼핑몰 구축
**[sekmall.com](https://sekmall.com) ・ 메인 담당(단독)**

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
**[koreanpsychology.or.kr](https://koreanpsychology.or.kr) ・ 서브 담당**

- 모학회 + 분과학회 통합 **회원 5~6만 명** 규모
- 회원 등급 체계, 연회비 · 가입비 정산, 결제 시스템 개발
- 학술행사 지원 · 신청 관리 기능 개발
- 분과별로 회비 정책이 달라 등급 · 분과 · 회비를 분리 설계하여 정책 변경에 대응

`PHP` `MySQL` `결제 API`

---

### ⚾ 명지전문대 KBO 야구심판 양성과정 — 교육 플랫폼
**[baseball.mjc.ac.kr](https://baseball.mjc.ac.kr) ・ 메인 담당**

- 수강생 회원 가입 및 관리
- 교육 과정 개설 · 신청 기능, 기수 · 정원 관리
- 게시판, 수료 자격증 발급 기능 개발

`PHP` `MySQL`

---

### 🎓 스펙트럼KU — 교육 플랫폼 + 국내외 결제
**[spectrumku.com](https://spectrumku.com) ・ 메인 담당**

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
| **대학 · 교육** | 고려대학교(경영대학 · 공과대학 · 의과대학 · 보건과학대학 외), 경희대학교(경영대학원 · 글로벌미래교육원 · AI비즈니스MBA 외), 서울대학교(SSBT · SSRT 외), 명지전문대학, 경기대학교, 한국원자력연구원(RCARO) |
| **대기업 · 제조** | HD현대오일뱅크, 현대케미칼, 현대쉘베이스오일, 현대오일터미널, 슈나이더일렉트릭코리아, 티케이엘리베이터코리아, 롯데베르살리스 엘라스토머스, 아남전자, 덕신하우징 |
| **협회 · 학회** | 한국심리학회, 한국석유화학협회, 한국제지연합회, 한국화학섬유협회, 한국광고주협회, 한국경영과학회, 국제경영원, 항공우주정책연구원, 공군사관학교총동창회 |
| **의료** | 고려대학교의료원(부정맥), 삼성서울병원 순환기내과, 서울아산병원 부정맥센터, 강동미즈여성병원, 사과나무치과병원, 온세메디칼 |
| **건설 · ERP** | 신동아건설, 대지건설, 보성건설, 금강인프라건설, 정안건설, 선풍토건, 일해토건 (다수 ERP 시스템 포함) |
| **쇼핑몰 · 커머스** | 에쓰오일 포인트몰 · 파트너몰, GS파트너몰, SEKMALL, 더푸짐, 한의바이오 |
| **공공** | 강북구청(생활지리정보 · 여성정보), 경주시장애인체육회, 월드비전 경기남지부 |

<details>
<summary><b>전체 유지보수 사이트 목록 펼쳐 보기</b></summary>

#### 대학 · 교육기관
```
고려대학교 경영대학, biz.korea.ac.kr
고려대학교 경영대학 (BK21), biz.korea.ac.kr/bk21four
고려대학교 경영대학 (CDC), biz.korea.ac.kr/cdc
고려대학교 경영대학 (ESG), esg.korea.ac.kr
고려대학교 경영대학 (랭킹), kubsrankings.korea.ac.kr
고려대학교 경영대학 (AICG), www.aicg.org
고려대학교 경영대학 (ASIA MBA), www.s3-asiamba.com
고려대학교 공과대학, eng.korea.ac.kr
고려대학교 공학대학원, enggra.korea.ac.kr / ceo.korea.ac.kr
고려대학교 기계공학부, me.korea.ac.kr
고려대학교 전기전자공학부, ee.korea.ac.kr
고려대학교 차세대통신학과, ce.korea.ac.kr
고려대학교 반도체공학과, se.korea.ac.kr
고려대학교 건축학과, archi.korea.ac.kr
고려대학교 건축학과 교우회, kua1964.com / kua1964.kr
고려대학교 미디어대학, mediacom.korea.ac.kr
고려대학교 보건과학대학, chs / bmeng / bsm / hes / hpm .korea.ac.kr
고려대학교 의과대학, kumstp.korea.ac.kr
고려대학교 MRC 마이오카인 융합연구센터, myokinemrc.korea.ac.kr
고려대학교 아세아문제연구원, asiaticresearch.org
고려대학교 지속가능원, sustainability / kusr / kusso .korea.ac.kr
고려대학교 대학원혁신본부, graduate.korea.ac.kr
고려대학교 KU-KIST융합대학원, kukistschool.korea.ac.kr
고려대학교 기업산학연협력센터, uric.korea.ac.kr
고려대학교 인권·성평등센터, humanrights.korea.ac.kr
고려대학교 VLSISP Lab., vlsisp.korea.ac.kr
경희대학교 경영대학원, khmba / wmba / emba / asp / mil / golf / ceo .khu.ac.kr
경희대학교 경영대학원(중국), khmbachina.khu.ac.kr
경희대학교 총동문회(경영대학원), kyungheemba.com
경희대학교 경영연구원, mri.khu.ac.kr
경희대학교 글로벌미래교육원, kaca / cce / ccea / ccek / klc / air / beauty / mamp / practicaldance .khu.ac.kr
경희대학교 AI 비즈니스MBA, aimba.khu.ac.kr / smartlab.khu.ac.kr
경희대학교 빅데이터응용학과, bigdata21.khu.ac.kr / bk21bigdata.khu.ac.kr
경희대학교 국제대학원, gsp.khu.ac.kr
경희대학교 일본로컬문화연구회, japanlocal.khu.ac.kr
서울대학교 SSBT(차세대이차전지), ssbt.snu.ac.kr
서울대학교 Advanced Energy Materials Lab, energylab.snu.ac.kr
서울대학교 SSRT, ssrt.snu.ac.kr
명지전문대학 평생교육원, edu.mjc.ac.kr
명지전문대학 야구심판양성과정, baseball.mjc.ac.kr
명지전문대학 조기취업형계약학과, early.mjc.ac.kr
명지전문대학 MRCC, mrcc.mjc.ac.kr
경기대학교, kgumie.com
안양대학교 평생교육원, ay.fiart.kr
한국원자력연구원(RCARO), e-campus.rcaro.org
```

#### 대기업 · 제조
```
HD현대오일뱅크(주), oilbank.co.kr / oilbankbiz.com / oilbankbiz.net
HD현대오일뱅크(주) 고객자문단, ob.oilbank.co.kr / advice.oilbank.co.kr
HD현대오일뱅크(주) 서울지점, shop.oilbankbiz.com
현대케미칼(주), www.hyundaichemical.co.kr
현대쉘베이스오일(주), hsbaseoil.co.kr / hsbaseoil.com
현대코스모(주) 서울지점, hyundaicosmo.com
현대오일터미널(주), www.oilterminal.co.kr
(재)HD현대일퍼센트나눔재단, hdhyundainanum.or.kr / honor.hdhyundainanum.or.kr
(재)HD현대희망재단, hdhyundaihope.org
현대네트웍스(주), hdnetworks.co.kr / flucare.co.kr
슈나이더일렉트릭코리아(주), schneider-electric.co.kr / service-frame-kr.se.com
티케이엘리베이터코리아(주) IGAD, igad-dev.tkek.co.kr / rigad-dev.tkek.co.kr
티케이엘리베이터코리아(주) TIS, customer.tkek.co.kr
롯데베르살리스 엘라스토머스(주), lvelastomers.com
아남전자(주), aname.co.kr / anamglobal.com / anamworldwide.com
(주)덕신하우징 · 덕신이피씨, duckshin.com / dukshinepc.com / duckshinvina.com
디에스인터내셔널(주), dsint.net / duckshinint.com
대한제지(주), www.daehanpaper.com
군자출판사(주), koonja.co.kr / smarteduk.co.kr / www.medicalpictures.co.kr / www.mediteriumart.com
(주)파블로항공, www.pabloair.com
다스코리아(주), daskorea.co.kr
```

#### 협회 · 학회 · 연구기관
```
(사)한국심리학회, koreanpsychology.or.kr / koreanpsychology.kr
(사)한국심리학회 재난심리위원회, dp.koreanpsychology.or.kr
서울시광역심리지원센터, mt.koreanpsychology.or.kr
한국석유화학협회, kpia.or.kr / ilovechem.kr / ilovechem.co.kr
한국제지연합회, paper.or.kr / ilovepaper.org
한국화학섬유협회, kcfa.or.kr
한국화학산업연합회, kocic.or.kr
한국화학소재기술연구조합, chemtra.or.kr
한국RC협의회, krcc.or.kr / hichem.or.kr / aprcc2019.com
(사)한국가스연맹, kgu.or.kr
(사)국제경영원, imi.or.kr / newhrd.com / member.imi.or.kr / online.imi.or.kr / forum.imi.or.kr
(사)한국광고주협회, kaa.or.kr
(사)한국경영과학회, komsri.kr / komsri.co.kr / komsri.or.kr
(사)한국의료행정실무협회, simsa.kr / cyber.simsa.kr
한국과학기술출판협회, kstpa.or.kr / mall.kstpa.or.kr
한국소비자광고심리학회, kscap.co.kr
사단법인 항공우주정책연구원, kapi.or.kr
(사)대한민국공군발전협회, arokaf.co.kr
공군사관학교총동창회, kafaaa.or.kr
공군인터넷전우회(로카피스), rokafis.or.kr / kafi.net
(사)로카피스생활체육회, rokafis.com
(재)한국지식재산관리재단, kipf.or.kr
(재)한국문화예술진흥재단, koracf.or.kr
한국당뇨협회, dangnyo.or.kr
한국출판인산악회, kpmclub.com
성우안보전략연구원, www.starflag.or.kr
(사)성무안보연구소, www.srins.re.kr
씨엠알기술연구원(주), cmr.or.kr
(재)한경협중소기업협력센터, www.fkilsc.or.kr
재단법인 무봉, mubong.org
```

#### 의료 · 병원 · 한의원
```
고려대학교의료원(부정맥), ep.kumc.or.kr / korea-heartrhythm.com
고대 심장혈관 연구소, cwri.co.kr
고려대학교의료원(흉통), koreaheart.co.kr
삼성서울병원 순환기내과, arrhythmia.co.kr
아산병원 부정맥센터, amc-heartrhythm.com
강동미즈여성병원, gmh.or.kr
사과나무치과병원, appledental.kr
랩케어진단검사의학과의원, labcare.kr
(주)온세메디칼, onsemedical.co.kr / medtrics.co.kr / clamed.co.kr / insui.co.kr / snamd.com
신진메딕스(주), diakey.com
평강한의원, daligra.com / 55clinic.com / seeok.co.kr
영도한의원, ydh.kr / china.ydh.kr
사하한의원, sahaclinic.co.kr / antipain.net / energyclinic.kr
정원한의원, stepdiet.net / stepdiet.co.kr
한중한의원, hjclinic.co.kr
김주성한의원, kjsclinic.co.kr
한상훈한의원, dr-han.co.kr
노메스한의원, nomes.seeok.co.kr
한방당뇨네트워크 / 당큐, dangclinic.com / dangclinic.co.kr
(주)한방케어, hanbangcarecar.co.kr / carecar.co.kr / 10care.co.kr
(주)한의바이오, hanibio.kr / hanibio.co.kr / dr-yakcho.co.kr
한의부항학회(한의바이오), k-act.or.kr
하니동물병원, animaltrap.co.kr / dogdr.co.kr
```

#### 건설 · ERP
```
신동아건설(주), sdaconst.co.kr / familie.co.kr / familieapt.co.kr
(주)대지건설, daejienc.co.kr / daejienc.com / erp.daejienc.com
보성건설(주), bosung21.com
선풍토건(주), sunpoong.co.kr / erp.sunpoong.co.kr
선주토건(주), sunjoo21.com
(주)일해토건, ilhae21.com / erp.ilhae21.com
금강인프라건설(주), kgcon.kr / erp.kgcon.kr
(주)정안건설, jaenc.kr / erp.jaenc.kr
(주)신흥건설, shin-heung.com / shdnc.co.kr
리코이엔씨(주), byuksong.co.kr / reeco.co.kr
삼구건설(주), 39c.co.kr
지에스건설(주), gongse.co.kr
신산SS토건(주), sinsan.co.kr
(주)이본종합건설, pajuhuton.com / pajuhuton.co.kr
삼삼엔지니어링(주), samsam.biz
씨티에스엔지니어링(주), ctseng.com
(주)한성리소스산업, erp.hs-recycling.com
(유)우양자원, wy-recycling.kr / erp.wy-recycling.kr
가나철거공사, gn7904.com
동화예건(주), dw.inhuedeco.co.kr
(주)인휴, inhuedeco.co.kr / ih.inhuedeco.co.kr
역북지역주택조합, yukbuk.co.kr
신길5동지역주택조합, singil5.com
서울대역편백숲1차지역주택조합, healing-state.co.kr / healingstate.co.kr
(주)커뮤니케이션소리 (분양), botanicparktower.co.kr / metrocity2.co.kr / ryumatower.co.kr / mabukutovill.co.kr
(주)포유, familie-gangdong.co.kr / familie-terraza.com / viewsky.co.kr
(주)인터크레존, daelim-acrotel.co.kr
```

#### 쇼핑몰 · 커머스
```
(주)에스엔유티씨엔티, sekmall.com / sekmall.co.kr / eocrmall.com / snutcnt.com
더푸짐주식회사, deopujim.com / inifood.co.kr
에쓰오일 포인트몰(한백산), mall.s-oilbonus.com / soil.hbsan.com
에쓰오일 파트너몰(한백산), s-partner.s-oil.com
GS파트너몰(한백산), with-partnermall.com
(주)한백산, hbsan.com / shop.hbsan.com / intranet.hbsan.com / elohas.co.kr / siru.co.kr
(주)그로넷테크놀러지, giftzone.oilbankcard.com
(주)이솝, ysop.co.kr / mall.ysop.co.kr
성준전기(주), sungjoon.co.kr / mall.sungjoon.co.kr
(주)하나일렉트릭, www.hnec.co.kr / mall.hnec.co.kr
유한메카트로닉스(주), mall.yu-han.co.kr
올웨이즈앤애프앤비(주), drstuarts.co.kr / drstuartshop.co.kr
(주)세계로물산, plows.co.kr / isaacfood.co.kr
고려콜렉션, korea-col.co.kr
미인나라, mi-in.co.kr / miinsoo.com
웰리스다이어트(쑥나린), ssuknarin.com
다앤미, 55diet.com
탐나는아동복탑랜드상가운영회, seoultopland.co.kr
```

#### 공공 · 기타 기업
```
강북구청(생활지리정보), wgis.gangbuk.seoul.kr
강북구청(여성정보), women.gangbuk.go.kr
경주시장애인체육회, gyeongjusad.or.kr
월드비전 경기남지부, wvgyeonggi.or.kr
피아트SID(주), fiart.net / fiart.kr / gw.fiart.kr / ezgw.fiart.kr / ezhrms.fiart.kr / easyerp.kr / message.fiart.kr
(주)피아트코리아, fiart.co.kr
(주)에스에이치글로벌, shglobal.kr / shglobal.co.kr / hrms.shglobal.kr
(주)텔레컨스, telecons.co.kr / mapzin.co.kr / rubie.co.kr / mcon-service.azurewebsites.net
(주)하이큐시스템, hiqsys.co.kr / hpsvc.kr / hpzone.co.kr
(주)에이치티엠, ho.htmco.kr / dtsys.kr / internet-korea.kr / lucky7.co
(주)비포시스템, bfsystem.kr / be4.co.kr / mgit.co.kr
(주)씨엘뱅크, clb.co.kr / pluscar.clb.co.kr
(주)한국기독교정보, christland.net / christinfo.co.kr
(주)한국티이아이, teikorea.com
(주)한국이엔아이인터네셔널, messeworld.co.kr
(주)디텍, incdt.net
(주)디케씨코퍼레이션, dkcor.com
(주)크레온유니티, icreon.co.kr
(주)지투디앤씨, g2dnc.co.kr / g2dnc.com / goldenfeetcnd.co.kr
지엔지주식회사, gng-steel.co.kr
(주)유니디아, unidia.co.kr / summit-tech.co.kr
(주)트라이텍코리아, triteckorea.co.kr
(주)한산기연, hansaneng.co.kr
동광기연(주), dktec.co.kr
동광리어유한회사, dklear.com
(주)한국건드릴, gundrill.co.kr
한국김치플랜트산업(주), kimchiplant.co.kr / kimchimachine.co.kr
(주)제이원모터스, hondacarsj-one.co.kr
JPC오토모티브, jwpre.com
제이와이커스텀(주), jycustom.com / jymap.co.kr
(주)에너넷, iener.net
(주)엘제이하이테크, lj-hitech.co.kr
(주)에이엔케이이노베이션, ankinnovation.com
(주)비앤드브이, multiflooring.com / floorcovering.co.kr / flooringcatalogue.com
(주)디자인벽지, designwallpaper.co.kr
(주)쉬스케미칼컨설팅, sheschem.com / loa.sheschem.com
(주)디앤에프, decknfuture.com
티엔에스슈퍼데크, tnssuperdeck.com
(주)한성로지스, hs-logis.co.kr
한신자원산업, h-shin.kr
(주)세문, semun.co.kr
(주)모노커뮤니케이션즈, mono.co.kr
(주)커뮤니케이션소리, lucebr.co.kr / wg3.co.kr / biz.hausd.co.kr
커뮤니케이션즈 리치(주), botanicparktower.co.kr
아티크스튜디오(주), artiquestudio.co.kr
(주)미디어비엠코리아, gogobm.co.kr / gogobm.com / gogobm.net / gogobm.kr
(주)더블유오케이, romadalgujitour.com
폰타나리조트, fontana-resort.co.kr / fontana-resort.kr
영천레포츠(주), www.exposkyfly.co.kr
(주)양음스탁119, st119.com
귀천(주), 1668-0000.co.kr / .com / .net
해피텔레콤, happy-tel.com / hms.happy-tel.com
노블레스싱글텔, nbtel.co.kr
(주)이슈텔레콤, is-telecom.co.kr
애니콤정보통신(주), anycomm.net
서경정보통신, kt-megapass.net
(주)케이티엘솔루션, kt-service.co.kr
(주)드림텔레시스, dtsys.kr
(주)고우넷, itsm.gownet.com
아이디비넷(주), yesas.co.kr
(주)디에스엘, globaldsl.co.kr
(주)지앤티글로벌, gntglobal.com
(주)버킷인터내셔날, bucketint.co.kr
(주)네트인, netin.kr
새론네트웍스, saeronnetworks.com
주식회사 다우시스, dowsys.co.kr / dowsys.net / polynaru.com
(주)컴투프리테크, comtopritech.co.kr
(주)이알씨라인, ercline.com
(주)유엔터스, uenters.com
(주)벨루션네트웍스, bellution.com
피지피기술(주), pgptech.co.kr
대명리프트, dmrental.co.kr
보임서비스(주), voimservice.com
(주)티에스비즈텍, tsbiz.net
혜성씨앤씨(주), hscnci.com
법무법인 온누리, onnurilaw.com
삼주공인노무사사무소, sjoffice.co.kr
글로북스, gbooks.kr
생명교회, lifegiving.or.kr
모새골, heart.pe.kr
달빛소리 영농조합법인, mv01.co.kr
이웃사랑임대사랑 사회적협동조합
강아지농장, skpet.co.kr
유벨라, ubella.co.kr / ubella.kr
눈치코치, seeok.co.kr / s-ok.co.kr
지에이시(GAC) 닥터아토앤비, atopyskin114.com
주식회사 이던인터내셔날, eathun.co.kr
(주)도담이앤씨종합건축사무소, dodam.fiart.kr
SAMKOO Vina, samkoo.fiart.kr
```

</details>

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
| 2016.09 | 전자기기기능사 | 한국산업인력공단 |

**학력** — 학점은행제 정보처리학과 재학 중 (2026.08 ~) · 서울전자고등학교 전자과 졸업
