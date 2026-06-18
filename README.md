# LLM Wiki Template

> 참고: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

선별한 원천 자료를 바탕으로 LLM이 유지하는 개인용 위키를 만들기 위한 템플릿 저장소다.

## 구조

```text
.
├── AGENTS.md
├── docs/
│   ├── commit-convention.md  # 샘플 커밋 컨벤션
│   └── llm-wiki/             # Andrej Karpathy의 LLM Wiki gist
│       ├── idea.en.md        # 원문
│       └── idea.ko.md        # 한국어 번역
└── llm-wiki/
    ├── AGENTS.md
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

`llm-wiki/`가 실제 복사 단위다. 다른 프로젝트에서 쓰려면 이 폴더를 프로젝트 안으로 복사한다.

## 사용법

1. 대상 프로젝트에 `llm-wiki/` 폴더를 복사한다.
2. 원천 문서를 `llm-wiki/raw/sources/`에 넣는다.
3. LLM 에이전트에게 `llm-wiki/AGENTS.md`를 기준으로 수집하거나 질문하라고 명시한다.
4. 생성된 위키는 `llm-wiki/wiki/index.md`에서 탐색한다.

Codex나 Claude 같은 에이전트가 프로젝트 루트의 지침 파일만 자동으로 읽는다면, 루트 지침 파일에서 `llm-wiki/AGENTS.md`를 따르라고 위임한다.

`docs/`는 템플릿 사용자를 위한 샘플 커밋 컨벤션과 LLM Wiki 아이디어 배경 자료다. 템플릿을 다른 프로젝트로 가져갈 때는 보통 `docs/`를 복사하지 않는다.
