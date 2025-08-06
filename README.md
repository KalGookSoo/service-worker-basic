# service-worker-basic
서비스 워커 기초

## 목차
### [Chapter 01 서비스 워커 소개](#chapter-01-서비스-워커-소개)

#### [01-1 서비스 워커란 무엇인가](chapters/01-1_what_is_service_worker.md)
- 서비스 워커의 정의와 역할
- 웹 개발자가 서비스 워커를 알아야 하는 이유
  - 오프라인 웹 경험 제공
  - 성능 최적화 및 사용자 경험 향상
- 서비스 워커와 웹 워커의 차이점
- 3가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [01-2 서비스 워커의 특징](chapters/01-2_service_worker_characteristics.md)
- 자바스크립트 워커 스레드
- 프록시 역할
- 이벤트 기반 아키텍처
- 비동기적 특성
- HTTPS 필수 요구사항
- 5가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [01-3 서비스 워커 지원 환경](chapters/01-3_service_worker_support.md)
- 브라우저 호환성
  - 데스크톱 브라우저
  - 모바일 브라우저
- 폴리필과 대체 방안
- 기능 감지 방법
- 4가지 키워드로 정리하는 핵심 포인트
- 확인 문제

### [Chapter 02 서비스 워커 생명주기](#chapter-02-서비스-워커-생명주기)
#### [02-1 서비스 워커 등록과 설치](chapters/02-1_registration_installation.md)
- 서비스 워커 스크립트 작성
- 서비스 워커 등록 과정
  - navigator.serviceWorker.register()
  - 스코프 설정
- 설치 이벤트 처리
  - install 이벤트
  - skipWaiting() 메서드
- 디버깅 및 문제 해결
- 5가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [02-2 서비스 워커 활성화와 업데이트](chapters/02-2_activation_update.md)
- 활성화 이벤트 처리
  - activate 이벤트
  - clients.claim() 메서드
- 서비스 워커 업데이트 메커니즘
  - 자동 업데이트
  - 수동 업데이트
- 버전 관리 전략
- 4가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [02-3 서비스 워커 상태 관리](chapters/02-3_state_management.md)
- 서비스 워커 상태 확인
  - ServiceWorkerRegistration 객체
  - ServiceWorker 객체
- 상태 변경 이벤트 처리
- 서비스 워커 제거 및 해제
- 4가지 키워드로 정리하는 핵심 포인트
- 확인 문제

### [Chapter 03 서비스 워커와 캐싱](#chapter-03-서비스-워커와-캐싱)
#### [03-1 Cache API 기초](chapters/03-1_cache_api_basics.md)
- Cache API 소개
- 캐시 스토리지 작업
  - 캐시 열기
  - 캐시에 응답 저장
  - 캐시에서 응답 검색
  - 캐시 항목 삭제
- 캐시 스토리지 관리
- 6가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [03-2 캐싱 전략](chapters/03-2_caching_strategies.md)
- 캐시 우선 전략 (Cache First)
- 네트워크 우선 전략 (Network First)
- 캐시 전용 전략 (Cache Only)
- 네트워크 전용 전략 (Network Only)
- 스테일-와일-리밸리데이트 전략 (Stale-While-Revalidate)
- 캐시 폴백 전략 (Cache Fallback)
- 적절한 전략 선택 방법
- 7가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [03-3 동적 콘텐츠 캐싱](chapters/03-3_dynamic_content_caching.md)
- API 응답 캐싱
- 조건부 캐싱
- 캐시 만료 및 갱신
- 헤더 기반 캐싱 결정
- 5가지 키워드로 정리하는 핵심 포인트
- 확인 문제

### [Chapter 04 서비스 워커 이벤트 처리](#chapter-04-서비스-워커-이벤트-처리)
#### [04-1 Fetch 이벤트](chapters/04-1_fetch_event.md)
- Fetch 이벤트 소개
- 요청 가로채기
- 응답 생성 및 수정
- 조건부 응답 처리
- 5가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [04-2 Push 이벤트와 알림](chapters/04-2_push_notifications.md)
- 웹 푸시 API 소개
- 푸시 서비스 구독
- 푸시 메시지 수신 및 처리
- 알림 표시 및 사용자 상호작용
- 6가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [04-3 백그라운드 동기화](chapters/04-3_background_sync.md)
- 백그라운드 동기화 API
- 동기화 이벤트 등록
- 오프라인 데이터 처리
- 재시도 메커니즘
- 4가지 키워드로 정리하는 핵심 포인트
- 확인 문제

### [Chapter 05 프로그레시브 웹 앱(PWA)](#chapter-05-프로그레시브-웹-앱)
#### [05-1 PWA 개요](chapters/05-1_pwa_overview.md)
- PWA의 정의와 특징
- PWA의 핵심 구성 요소
  - 서비스 워커
  - 매니페스트 파일
  - HTTPS
- PWA의 장점과 한계
- 4가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [05-2 매니페스트 파일](chapters/05-2_manifest_file.md)
- Web App Manifest 소개
- 매니페스트 파일 구성
  - 기본 정보 설정
  - 아이콘 설정
  - 디스플레이 모드
  - 시작 URL 및 방향
- 홈 화면 설치 경험 최적화
- 5가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [05-3 오프라인 경험 구현](chapters/05-3_offline_experience.md)
- 오프라인 페이지 설계
- 오프라인 상태 감지
- 오프라인 데이터 저장 및 동기화
- 사용자 경험 최적화
- 4가지 키워드로 정리하는 핵심 포인트
- 확인 문제

### [Chapter 06 서비스 워커와 프레임워크](#chapter-06-서비스-워커와-프레임워크)
#### [06-1 React에서 서비스 워커 활용](chapters/06-1_service_workers_in_react.md)
- Create React App의 서비스 워커
- Workbox와 React 통합
- React 애플리케이션에서 PWA 구현
- 상태 관리와 서비스 워커 통신
- 5가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [06-2 Workbox 라이브러리](chapters/06-2_workbox_library.md)
- Workbox 소개
- 주요 모듈 및 기능
  - 라우팅
  - 캐싱 전략
  - 프리캐싱
  - 백그라운드 동기화
- 빌드 도구 통합
- 6가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [06-3 Java 백엔드와 서비스 워커 연동](chapters/06-3_java_backend_integration.md)
- 서버 푸시 구현
- Spring Boot와 웹 푸시 연동
- 푸시 알림 서버 구축
- 보안 및 인증 처리
- 5가지 키워드로 정리하는 핵심 포인트
- 확인 문제

### [Chapter 07 서비스 워커 고급 주제](#chapter-07-서비스-워커-고급-주제)
#### [07-1 성능 최적화](chapters/07-1_performance_optimization.md)
- 리소스 우선순위 지정
- 프리캐싱과 런타임 캐싱
- 네트워크 요청 최적화
- 성능 측정 및 모니터링
- 5가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [07-2 보안 고려사항](chapters/07-2_security_considerations.md)
- HTTPS 요구사항
- 서비스 워커 스코프 제한
- 중요 데이터 처리
- 보안 모범 사례
- 4가지 키워드로 정리하는 핵심 포인트
- 확인 문제

#### [07-3 디버깅 및 테스트](chapters/07-3_debugging_testing.md)
- 브라우저 개발자 도구
  - Chrome DevTools
  - Firefox DevTools
- 서비스 워커 디버깅 기법
- 자동화된 테스트 방법
- 일반적인 문제 해결
- 5가지 키워드로 정리하는 핵심 포인트
- 확인 문제

### [정답 및 해설](answers_and_explanations.md)
### 찾아보기
