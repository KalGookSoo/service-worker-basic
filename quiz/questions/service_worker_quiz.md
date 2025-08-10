# 서비스 워커 기초 기출문제

이 문서는 서비스 워커 기초에 관한 25개의 기출문제를 포함하고 있습니다. 각 문제는 단일 응답 또는 복수 응답 객관식 문제로 구성되어 있습니다.

## 목차
- [서비스 워커 소개](#서비스-워커-소개)
- [서비스 워커 생명주기](#서비스-워커-생명주기)
- [서비스 워커와 캐싱](#서비스-워커와-캐싱)
- [서비스 워커 이벤트 처리](#서비스-워커-이벤트-처리)
- [프로그레시브 웹 앱(PWA)](#프로그레시브-웹-앱pwa)
- [서비스 워커 고급 주제](#서비스-워커-고급-주제)

## 서비스 워커 소개

### 문제 1
**문제**: 서비스 워커의 가장 기본적인 특성은 무엇인가요?
- [ ] 메인 스레드에서 실행된다
- [ ] DOM에 직접 접근할 수 있다
- [ ] 브라우저와 네트워크 사이에서 프록시 역할을 한다
- [ ] 동기적으로 작동한다

### 문제 2
**문제**: 서비스 워커를 사용하기 위해 반드시 필요한 프로토콜은 무엇인가요? (개발 환경 제외)
- [ ] HTTP
- [ ] HTTPS
- [ ] FTP
- [ ] WebSocket

### 문제 3
**문제**: 서비스 워커와 웹 워커의 차이점으로 올바른 것을 모두 고르세요.
- [ ] 서비스 워커는 페이지가 닫힌 후에도 실행될 수 있다
- [ ] 웹 워커는 DOM에 직접 접근할 수 있다
- [ ] 서비스 워커는 네트워크 요청을 가로챌 수 있다
- [ ] 서비스 워커는 여러 페이지에서 공유될 수 있다
- [ ] 웹 워커는 HTTPS 없이도 사용할 수 있다

### 문제 4
**문제**: 다음 중 서비스 워커 지원 여부를 확인하는 올바른 코드는?
- [ ] `if (window.serviceWorker) { ... }`
- [ ] `if ('serviceWorker' in navigator) { ... }`
- [ ] `if (document.serviceWorker) { ... }`
- [ ] `if (browser.supportsServiceWorker()) { ... }`

## 서비스 워커 생명주기

### 문제 5
**문제**: 서비스 워커의 생명주기 상태 중 올바른 순서는?
- [ ] 설치(installing) → 대기(waiting) → 활성화(activating) → 활성(active)
- [ ] 등록(registering) → 설치(installing) → 활성화(activating) → 활성(active)
- [ ] 다운로드(downloading) → 설치(installing) → 활성화(activating) → 활성(active)
- [ ] 등록(registering) → 다운로드(downloading) → 설치(installing) → 활성(active)

### 문제 6
**문제**: 서비스 워커 설치 중에 리소스를 미리 캐싱하는 이벤트는?
- [ ] activate
- [ ] fetch
- [ ] install
- [ ] message

### 문제 7
**문제**: 서비스 워커 스크립트가 업데이트되었을 때 즉시 활성화하기 위해 사용하는 메서드는?
- [ ] self.activate()
- [ ] self.skipWaiting()
- [ ] self.update()
- [ ] self.forceActivate()

### 문제 8
**문제**: 서비스 워커 등록 시 스코프를 지정하는 올바른 방법은?
- [ ] `navigator.serviceWorker.register('/sw.js', { path: '/app/' })`
- [ ] `navigator.serviceWorker.register('/sw.js', { scope: '/app/' })`
- [ ] `navigator.serviceWorker.register('/sw.js', { directory: '/app/' })`
- [ ] `navigator.serviceWorker.register('/app/sw.js')`

### 문제 9
**문제**: 새로 설치된 서비스 워커가 활성화된 후 모든 클라이언트를 즉시 제어하도록 하는 메서드는?
- [ ] self.takeControl()
- [ ] clients.claim()
- [ ] self.claimClients()
- [ ] navigator.serviceWorker.claim()

## 서비스 워커와 캐싱

### 문제 10
**문제**: Cache API에서 캐시를 열거나 생성하는 메서드는?
- [ ] caches.create()
- [ ] caches.get()
- [ ] caches.open()
- [ ] caches.init()

### 문제 11
**문제**: 다음 중 서비스 워커에서 사용할 수 있는 캐싱 전략이 아닌 것은?
- [ ] Cache First
- [ ] Network First
- [ ] Stale-While-Revalidate
- [ ] Server-Side Rendering

### 문제 12
**문제**: 네트워크 요청을 먼저 시도하고 실패할 경우 캐시에서 응답을 제공하는 전략은?
- [ ] Cache First
- [ ] Network First
- [ ] Cache Only
- [ ] Network Fallback

### 문제 13
**문제**: 다음 중 Cache API를 사용하여 캐시에 응답을 추가하는 올바른 코드는?
- [ ] `cache.put(request, response)`
- [ ] `cache.add(url)`
- [ ] `cache.store(request, response)`
- [ ] `cache.save(url, response)`

### 문제 14
**문제**: 캐시된 응답을 제공하면서 동시에 백그라운드에서 네트워크 요청을 통해 캐시를 업데이트하는 전략은?
- [ ] Cache First
- [ ] Network First
- [ ] Stale-While-Revalidate
- [ ] Cache Then Network

## 서비스 워커 이벤트 처리

### 문제 15
**문제**: 서비스 워커에서 네트워크 요청을 가로채는 데 사용되는 이벤트는?
- [ ] request
- [ ] fetch
- [ ] intercept
- [ ] network

### 문제 16
**문제**: 푸시 알림을 구현하기 위해 서비스 워커에서 처리해야 하는 이벤트는?
- [ ] push
- [ ] notification
- [ ] message
- [ ] alert

### 문제 17
**문제**: 백그라운드 동기화를 위해 서비스 워커에서 사용하는 이벤트는?
- [ ] background
- [ ] sync
- [ ] update
- [ ] offline

### 문제 18
**문제**: 서비스 워커에서 fetch 이벤트 처리 시 응답을 생성하는 방법으로 올바른 것을 모두 고르세요.
- [ ] 캐시에서 응답 반환
- [ ] 네트워크 요청으로 응답 생성
- [ ] Response 객체 직접 생성
- [ ] DOM 요소 반환
- [ ] Promise 반환

## 프로그레시브 웹 앱(PWA)

### 문제 19
**문제**: PWA의 필수 구성 요소가 아닌 것은?
- [ ] 서비스 워커
- [ ] 매니페스트 파일
- [ ] HTTPS
- [ ] 서버 사이드 렌더링

### 문제 20
**문제**: 웹 앱 매니페스트 파일의 확장자는?
- [ ] .manifest
- [ ] .webmanifest
- [ ] .json
- [ ] .pwa

### 문제 21
**문제**: 웹 앱 매니페스트에서 앱의 표시 모드를 지정하는 속성은?
- [ ] view
- [ ] mode
- [ ] display
- [ ] appearance

### 문제 22
**문제**: 오프라인 상태를 감지하는 JavaScript 이벤트는?
- [ ] window.onoffline
- [ ] navigator.onoffline
- [ ] window.addEventListener('offline', ...)
- [ ] document.onoffline

## 서비스 워커 고급 주제

### 문제 23
**문제**: 서비스 워커에서 중요한 리소스를 미리 캐싱하는 기법은?
- [ ] 런타임 캐싱
- [ ] 프리캐싱
- [ ] 동적 캐싱
- [ ] 지연 캐싱

### 문제 24
**문제**: 서비스 워커의 보안 관련 특성으로 올바른 것을 모두 고르세요.
- [ ] HTTPS 필수 요구사항
- [ ] 스코프 제한
- [ ] 샌드박스 환경에서 실행
- [ ] 사용자 인증 필수
- [ ] 동일 출처 정책 적용

### 문제 25
**문제**: 서비스 워커 성능 최적화 방법으로 올바르지 않은 것은?
- [ ] 필요한 리소스만 캐싱하기
- [ ] 적절한 캐싱 전략 선택하기
- [ ] 모든 네트워크 요청 차단하기
- [ ] 캐시 만료 정책 설정하기

> [정답 및 해설 보기](../answers/service_worker_quiz_answers.md)
