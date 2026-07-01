# 로그

위키 활동을 시간순으로 기록하는 추가 전용 로그다.

항목은 다음 형식을 사용한다.

```md
## [YYYY-MM-DD] ingest | 원천 자료 제목

- 원천 자료: `raw/sources/<category>/source-file.md`
- 업데이트: [[source-page]], [[concept-page]]
- 메모: 변경된 내용의 짧은 요약.

## [YYYY-MM-DD] query | 질문

- 질문: 사용자가 던진 질문.
- 참고: [[source-page]], [[concept-page]]
- 저장: [[question-page]]

## [YYYY-MM-DD] lint | 범위

- 점검 범위: `wiki/`
- 발견: 모순, 고아 페이지, 누락된 교차 참조, 데이터 공백.
- 후속 작업: 필요한 수정 또는 추가 원천 자료 후보.
```

## [2026-06-05] setup | 초기 템플릿 구조

- 기본 LLM Wiki 구조를 만들었다.
- 원천 자료, 위키, 템플릿, 도구 디렉터리를 추가했다.
