# LLM Wiki Template

> 참고: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

선별한 원천 자료를 바탕으로 LLM이 유지하는 개인용 위키를 만들기 위한 템플릿 저장소다.

## 구조

```text
.
├── AGENTS.md
├── docs/
│   ├── commit-convention.md
│   └── llm-wiki/
└── llm-wiki/
    ├── AGENTS.md
    ├── README.md
    ├── raw/
    ├── tools/
    └── wiki/
```

`llm-wiki/`가 실제 복사 단위다. 다른 프로젝트에서 쓰려면 이 폴더를 프로젝트 안으로 복사한다.

## 사용법

1. 대상 프로젝트에 `llm-wiki/` 폴더를 복사한다.
2. 원천 문서를 `llm-wiki/raw/sources/`에 넣는다.
3. LLM 에이전트에게 `llm-wiki/AGENTS.md`를 기준으로 수집하거나 질문하라고 요청한다.
4. 생성된 위키는 `llm-wiki/wiki/index.md`에서 탐색한다.

`docs/`는 이 저장소의 배경 설명과 커밋 규칙이다. 템플릿을 다른 프로젝트로 가져갈 때는 보통 복사하지 않는다.
