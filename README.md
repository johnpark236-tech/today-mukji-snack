# 오늘 뭐먹지? · 간식편

스마트폰에서 “오늘 어떤 간식 먹지?”를 빠르게 고르고, 초보자도 단계별로 따라 만들 수 있게 구성한 모바일 우선 간식 레시피 앱입니다.

## 주요 기능

- 오늘의 추천 간식
- 간식명·재료 검색
- 5분·10분·15분 및 카테고리 필터
- 단계별 조리 모드
- 현재 단계 / 전체 레시피 음성 안내 구조
- 장보기 목록
- 집에 있는 재료로 만들 수 있는 간식 추천
- PWA 모바일 UI
- 저장소 내부 SVG 대표 이미지 12장

## 기본 간식 12종

길거리 계란토스트, 프렌치토스트, 떡꼬치, 컵 떡볶이, 콘치즈, 고구마 맛탕, 버터 감자구이, 바나나 팬케이크, 과일 요거트볼, 라면땅, 컵 계란빵, 초코 머그케이크.

## 저장소 구조

- `assets/snacks/` — 간식 대표 이미지
- `data/recipes-fallback.json` — 간식 레시피 데이터
- `js/` — 검색·추천·조리·장보기·TTS 클라이언트
- `apps-script/` — 선택형 Google Apps Script API / Google Cloud TTS 백엔드
- `docs/` — 배포·TTS·데이터 관리 문서

## 로컬 실행

```bash
python -m http.server 8080
```

브라우저에서:

```text
http://localhost:8080/#/home
```

Google Apps Script URL이 설정되지 않은 상태에서도 로컬 fallback 레시피 데이터로 동작합니다.

## 보안

프런트엔드와 공개 저장소에는 API key, OAuth token, service-account JSON, GitHub token, 비밀번호 등 비밀정보를 저장하지 않습니다.
