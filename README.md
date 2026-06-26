# Scheduler

Material 3 스타일의 모바일 스케쥴러 PWA. 단일 HTML 파일로 동작하며, 설치형 앱처럼 사용할 수 있습니다.

## 기능
- **일정 / 할 일 / 반복 일정** 관리
- **주간표 · 하루 타임라인 · 원형 시계** 3가지 시간표 뷰
- **라이브 타이머**와 전체화면 **집중 모드**
- **주간 통계** (완료율 · 누적 시간)
- **알림** (일정 시작/종료 브라우저 알림)
- **클라우드 동기화** (Supabase, 선택)
- 오프라인 동작 (Service Worker 캐시) + 홈 화면 설치 (PWA)

## 실행
정적 파일이라 별도 빌드가 필요 없습니다. 로컬에서 보려면:

```bash
npx serve -p 3333 .
```

브라우저에서 `http://localhost:3333` 접속.

> Service Worker / PWA 설치는 `http(s)` 환경에서만 동작합니다 (`file://` 제외).

## 배포 (GitHub Pages)
1. 이 저장소를 GitHub에 푸시
2. **Settings → Pages → Source: `main` 브랜치 / `/ (root)`** 선택
3. 발급된 `https://<사용자>.github.io/<저장소>/` 에서 접속 후 "홈 화면에 추가"로 설치

## 클라우드 동기화 설정 (선택)
`index.html` 상단의 `SUPABASE_URL` / `SUPABASE_ANON_KEY` 를 본인 프로젝트 값으로 채우면 기기 간 동기화가 켜집니다. 비워두면 오프라인(localStorage)으로 동작합니다.
