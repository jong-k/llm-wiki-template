# LLM Wiki Template

> 참고: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

선별한 원천 자료를 바탕으로 LLM이 유지하는 위키를 만들기 위한 재사용 가능한 템플릿.

원시 자료는 불변으로 두고, LLM이 구조화된 마크다운 위키를 유지하게 하며, `AGENTS.md`를 운영 스키마로 사용한다.

## 구조

```text
.
├── AGENTS.md             # LLM Wiki 운영 스키마와 워크플로
├── README.md
├── raw/                  # 사용자가 선별한 불변 원천 자료
│   ├── README.md         # 원천 자료 관리 규칙
│   ├── assets/           # 이미지, 스크린샷, PDF, 첨부파일
│   └── sources/          # 기사, 노트, 녹취록, 내보내기 파일
├── tools/                # 선택적 헬퍼 스크립트와 로컬 검색 도구
│   └── README.md         # 도구 추가 기준과 예시
└── wiki/                 # LLM이 생성하고 유지하는 위키 본문
    ├── _templates/       # 위키 페이지 유형별 작성 템플릿
    ├── concepts/         # 아이디어, 이론, 용어, 패턴
    ├── entities/         # 사람, 조직, 제품, 장소 등 명명된 대상
    ├── questions/        # 오래 보존할 질문과 답변
    ├── sources/          # 원천 자료별 요약
    ├── syntheses/        # 여러 원천을 엮은 분석과 종합
    ├── index.md          # 위키 콘텐츠 카탈로그
    ├── log.md            # 위키 작업 기록
    ├── README.md         # 위키 디렉터리 안내
    └── overview.md       # 위키의 최상위 종합
```

## 빠른 시작

1. 원천 문서를 `raw/sources/`에 추가한다.
2. LLM 에이전트에게 `AGENTS.md`를 기준으로 원천 자료를 수집하라고 요청한다.
3. 생성된 위키를 `wiki/index.md`에서 탐색한다.
4. 오래 보존할 분석은 `wiki/syntheses/` 또는 `wiki/questions/`에 남긴다.

`raw/`는 사용자가 제공한 원천 자료를 위한 공간이다. `wiki/`는 LLM이 유지하는 지식을 위한 공간이다. `tools/`는 선택 사항이며, 검색이나 자동화가 필요해질 때까지 비워둬도 된다.
