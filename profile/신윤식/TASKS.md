# 신윤식 - 할 일 목록 (일 단위)

## 역할
- 백엔드 개발 (FastAPI)
- 클라우드 아키텍처 설계·구현
- API·인증·배포 파이프라인 구축

## 작업 레포지토리
- **Backend 레포지토리** (back 작업)

---

## 🚀 Day 1 (1/21 수): 프로젝트 초기 설정

### 프로젝트 초기 설정
- [ ] Backend 레포지토리 생성 및 FastAPI 프로젝트 구조 설계
- [ ] 의존성 관리 (requirements.txt, pyproject.toml)
- [ ] 환경 변수 관리 (.env 파일 구조)
- [ ] 로깅 시스템 설정
- [ ] 기본 FastAPI 앱 구조 생성

### 데이터베이스 기본 설정
- [ ] PostgreSQL 연결 설정 (또는 SQLite로 시작)
- [ ] SQLAlchemy ORM 설정
- [ ] 기본 연결 테스트

### 협업 준비
- [ ] Flutter 레포지토리(최성현)와 API 스펙 초안 협의
- [ ] Backend 레포지토리 내부 - 데이터 아키텍처(유재연)와 스키마 초안 협의
- [ ] API 문서화 도구 설정 (Swagger/OpenAPI)

---

## 🔐 Day 2 (1/22 목): 인증 시스템

### 인증 시스템 구축
- [ ] JWT 토큰 기반 인증 구현
- [ ] 비밀번호 해싱 (bcrypt)
- [ ] 회원가입 엔드포인트 (`POST /api/auth/register`)
- [ ] 로그인 엔드포인트 (`POST /api/auth/login`)
- [ ] 토큰 갱신 엔드포인트 (`POST /api/auth/refresh`)
- [ ] 사용자 프로필 조회 (`GET /api/users/me`)

### 기본 인프라
- [ ] 미들웨어 설정 (CORS, 에러 핸들링)
- [ ] API 문서화 (Swagger/OpenAPI) 기본 설정
- [ ] 입력 검증 (Pydantic)

---

## 🖼️ Day 3 (1/23 목): 옷장 관리 API

### 옷장 아이템 CRUD
- [ ] 아이템 추가 (`POST /api/wardrobe/items`)
- [ ] 아이템 조회 (전체/단일) (`GET /api/wardrobe/items`, `GET /api/wardrobe/items/{id}`)
- [ ] 아이템 수정 (`PUT /api/wardrobe/items/{id}`) - 기본
- [ ] 아이템 삭제 (`DELETE /api/wardrobe/items/{id}`)
- [ ] 카테고리별 필터링 (`GET /api/wardrobe/items?category={category}`)

### 이미지 처리
- [ ] 이미지 업로드 처리 API (`POST /api/wardrobe/items/upload`)
- [ ] 이미지 저장 전략 (로컬 저장소로 시작)
- [ ] 이미지 검증 (형식, 크기)
- [ ] 이미지 다운로드 (`GET /api/wardrobe/items/{id}/image`)

---

## 🔍 Day 4 (1/24 토): Vector DB 및 추천 API

### Vector DB 연동
- [ ] ChromaDB 또는 Postgres VectorDB 연결 설정
- [ ] Vector DB 검색 API 기본 구현
- [ ] 임베딩 저장/조회 API

### 코디 추천 API
- [ ] 오늘의 픽 조회 (`GET /api/recommendations/today`)
- [ ] 코디 재생성 (`POST /api/recommendations/regenerate`)
- [ ] 코디 상세 정보 조회 (`GET /api/recommendations/{id}`)

---

## 🤖 Day 5 (1/25 토): LLM 연동

### LLM 기본 연동
- [ ] GPT-4o API 연동 설정
- [ ] API 키 관리 및 환경 변수 설정
- [ ] API 호출 래퍼 함수 작성
- [ ] 에러 핸들링 및 재시도 로직 (기본)
- [ ] 프롬프트 호출 API

### 추천 설명 생성
- [ ] 추천 사유 생성 API
- [ ] LLM 응답 파싱 및 구조화

---

## 🌤️ Day 6 (1/26 월): 날씨 API 및 코디 상세

### 날씨 연동
- [ ] 날씨 API 연동 (`GET /api/weather/current`)
- [ ] 날씨 데이터 캐싱 (기본)

### 코디 상세 API
- [ ] 코디 상세 정보 API 완성
- [ ] 코디 히스토리 조회 (`GET /api/recommendations/history`) - 기본

---

## 🔄 Day 7 (1/27 화): 파이프라인 통합 및 최적화

### 추천 파이프라인 통합
- [ ] 추천 파이프라인 API 통합
- [ ] 전체 플로우 테스트
- [ ] 성능 최적화 (기본)

### 에러 처리
- [ ] 전역 에러 핸들링 개선
- [ ] 로깅 개선
- [ ] API 응답 시간 최적화

---

## 💬 Day 8 (1/28 수): AI 채팅 API

### 채팅 API
- [ ] 채팅 메시지 전송 (`POST /api/chat/message`)
- [ ] 채팅 히스토리 조회 (`GET /api/chat/history`)
- [ ] 채팅 세션 관리

### 스트리밍 (선택, 시간 여유 시)
- [ ] 기본 스트리밍 응답 구현 (SSE 또는 WebSocket)

---

## 🧪 Day 9 (1/29 목): 테스트 및 버그 수정

### 테스트
- [ ] 주요 API 엔드포인트 테스트
- [ ] 통합 테스트 (기본)
- [ ] 버그 수정
- [ ] 성능 테스트 (기본)

### 최적화
- [ ] 쿼리 최적화
- [ ] 응답 시간 개선
- [ ] 에러 처리 개선

---

## 🚀 Day 10 (1/30 금): 최종 통합 및 배포 준비

### 최종 작업
- [ ] 최종 통합 테스트
- [ ] API 문서 완성
- [ ] 배포 준비 (기본, 로컬 또는 간단한 클라우드)
- [ ] 환경 설정 가이드 작성

---

## 🔄 협업 포인트

### Flutter 레포지토리 (최성현)와 협의 필요
- [ ] API 스펙 정의 (Day 1)
- [ ] 인증 토큰 관리 방식 (Day 2)
- [ ] 이미지 업로드/다운로드 프로토콜 (Day 3)
- [ ] API 응답 형식 (지속적)

### Backend 레포지토리 내부 협의
- [ ] 데이터 아키텍처(유재연)와 데이터베이스 스키마 리뷰 (Day 1-2)
- [ ] 데이터 아키텍처(유재연)와 Vector DB 연동 방식 (Day 4)
- [ ] AI 엔지니어링(이강건)과 LLM API 호출 방식 (Day 5)
- [ ] AI 엔지니어링(이강건)과 Vector DB 검색 API 설계 (Day 4)
- [ ] AI 엔지니어링(이강건)과 프롬프트 관리 시스템 (Day 5)

---

## 📝 참고사항

- **우선순위**: 인증 → 옷장 관리 → Vector DB → LLM → 추천 → 채팅 순
- **완벽보다 완성**: 동작하는 API 우선
- **일일 커밋**: 매일 최소 1회 이상 커밋
- **빠른 통합**: 매일 저녁 Flutter 레포지토리와 통합 테스트
- **로컬 우선**: 클라우드 배포는 MVP 이후

---

*Last updated: 2026-01-21*
