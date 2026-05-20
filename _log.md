# LLM 위키 로그

## [2026-05-20] ingest | 온라인 유학원 인강 브랜딩 질문정리 PDF

- 원본 PDF에서 질문과 빨간색 답변을 추출해 `온라인 유학원 인강 브랜딩 질문정리.md`로 정리함.
- 홍승현 물리강사 브랜딩용 칼럼 정리본 `홍승현 물리강사 브랜딩 정리.md`를 생성함.
- 두 문서를 `raw/`에 원자료로 복사함.

## [2026-05-20] setup | Karpathy-style LLM Wiki

- Andrej Karpathy의 LLM Wiki Gist를 `references/karpathy-llm-wiki.md`에 저장함.
- `zhurudong/andrej-karpathy-llm-wiki` GitHub 저장소를 `references/github/andrej-karpathy-llm-wiki/`에 클론함.
- 홍승현 물리 인강 사업 목적에 맞게 `AGENTS.md`, `rules/위키 운영 규칙.md`, `wiki/_index.md`를 생성함.

## [2026-05-20] ingest | 엘리쌤 영어강사 브랜딩 질문정리

- 사용자 제공 텍스트를 `raw/2026-05-20-ellie-english-branding-qa.md`에 저장함.
- 엘리쌤을 English / Academic English 강사로 분리해 `people`, `brand`, `students`, `curriculum`, `content`, `sales`, `sources` 페이지를 생성함.
- Obsidian에서 엘리쌤 관련 페이지를 핑크색으로 구분할 수 있도록 `cssclasses: [ellie-pink]`와 `wiki/.obsidian/snippets/ellie-pink.css`를 추가함.

## [2026-05-20] ingest | 세현 플랫폼 브랜딩 질문정리

- 사용자 제공 텍스트를 `raw/2026-05-20-sehyun-platform-branding-qa.md`에 저장함.
- 세현은 강사가 아니라 국제학교 컨설팅 출신 기획자로 분리해 저장함.
- `people/세현`, `brand/플랫폼-브랜드-방향`, `brand/세현-기획-핵심가치`, `content/라이트보드-기반-강의`, `students/국제학교-개념적용-학생`, `sales/플랫폼-신뢰-포인트`, `sources/세현-플랫폼-브랜딩-질문정리`를 생성함.
- Obsidian에서 세현/기획 관련 페이지를 초록색으로 구분할 수 있도록 `cssclasses: [planning-green]`와 `wiki/.obsidian/snippets/planning-green.css`를 추가함.

## [2026-05-20] maintenance | 홍승현 태그 보강

- 홍승현 관련 페이지 10개에 `teacher: seunghyun`, `subject: physics`, `cssclasses: [physics-blue]`를 추가함.
- 홍승현 관련 페이지 10개에 `seunghyun`, `hong-seunghyun`, `승현`, `teacher-hong`, `physics` 태그를 추가함.
- Obsidian에서 홍승현/Physics 관련 페이지를 파란색으로 구분할 수 있도록 `wiki/.obsidian/snippets/physics-blue.css`를 추가함.

## [2026-05-20] maintenance | 홍승현 확장 분야 메시지 제거

- 홍승현 태그가 붙은 위키 페이지에서 Art, Business, Finance, Economics, Branding, Media 등 확장 분야로 Physics를 연결하는 메시지를 제거함.
- 홍승현 브랜딩 방향을 국제학교 Physics, 쉬운 이해, AP/GPA/시험 적용 중심으로 정리함.

## [2026-05-20] integration | Hermes Agent memory 연결

- Hermes Agent repo를 `tools/hermes-agent/`에 클론해 설치/구조를 확인함.
- 기존 `~/.hermes` 설치와 gateway 실행 상태를 확인함.
- Hermes `llm-wiki` 스킬 호환을 위해 `SCHEMA.md`를 생성하고 `index.md -> _index.md`, `log.md -> _log.md` 링크를 추가함.
- `~/.hermes/.env`에 `WIKI_PATH`와 `OBSIDIAN_VAULT_PATH`를 이 vault 경로로 설정함.
- `~/.hermes/config.yaml`의 `terminal.cwd`를 이 vault 경로로 설정함.
- `~/.hermes/skills/research/ivypath-wiki/SKILL.md`를 추가해 IvyPath 전용 위키 사용 규칙을 등록함.
- `~/.hermes/memories/MEMORY.md`에 IvyPath 위키를 먼저 읽으라는 기억을 추가함.
