# IvyPath Wiki Schema

## Domain

국제학교 학생 대상 온라인 강의 사업을 위한 기억 저장소다. 현재 주요 축은 홍승현 Physics, 엘리쌤 English / Academic English, 세현의 국제학교 컨설팅 기반 플랫폼 기획이다.

이 위키는 Obsidian vault이자 Hermes Agent의 `llm-wiki` 기억 저장소로 사용한다.

## Critical Orientation

질문에 답하기 전에 항상 다음 파일을 먼저 읽는다.

1. `AGENTS.md` 또는 이 `SCHEMA.md`
2. `_index.md` 또는 `index.md`
3. `_log.md` 또는 `log.md`

`index.md`는 `_index.md` 호환 링크이고, `log.md`는 `_log.md` 호환 링크다.

## Directory Map

| Folder | Purpose |
| --- | --- |
| `people/` | 강사, 기획자, 핵심 인물 |
| `brand/` | 브랜드 정의, 핵심가치, 포지셔닝 |
| `students/` | 국제학교 학생 페르소나, 고민, 감정, 학습 상황 |
| `curriculum/` | AP, IB, IGCSE, A-Level, GPA, SAT, TOEFL, Academic English |
| `content/` | 강의 방식, 라이트보드, 콘텐츠 구조 |
| `sales/` | 상세페이지, 광고, 학부모 설득, 결제 이유 |
| `sources/` | 원자료별 요약 |
| `raw/` | 변경하지 않는 원자료 |
| `queries/` | 재사용 가치가 있는 질문 답변 |

## Frontmatter Rules

모든 위키 페이지는 YAML frontmatter를 사용한다.

```yaml
---
type: person | brand | student | curriculum | content | sales | source | query
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: []
aliases: []
teacher:
subject:
person:
role:
cssclasses: []
source:
---
```

## Identity Tags

- 홍승현 Physics: `teacher: seunghyun`, `subject: physics`, `cssclasses: [physics-blue]`, tags include `seunghyun`, `hong-seunghyun`, `승현`, `teacher-hong`, `physics`
- 엘리쌤 English: `teacher: ellie`, `subject: english`, `cssclasses: [ellie-pink]`, tags include `ellie`, `english`, `international-school`
- 세현 Planner: `person: sehyun`, `role: planner`, `subject: platform-planning`, `cssclasses: [planning-green]`, tags include `sehyun`, `planning`, `consulting`, `lightboard`

## Query Rules

When answering user questions:

1. Read `_index.md` first.
2. Read 2-8 relevant linked pages.
3. If needed, search the vault with `rg`.
4. Answer from the wiki. If the wiki does not contain the answer, say so.
5. If the answer combines multiple pages into reusable strategy, save it under `queries/`, update `_index.md`, and append `_log.md`.

## Ingest Rules

When the user provides new notes, PDFs, or answers:

1. Save the original or cleaned source under `raw/`.
2. Create or update a source page under `sources/`.
3. Split durable ideas into small linked pages.
4. Keep 강사/기획자 identities separate.
5. Update `_index.md`.
6. Append `_log.md`.

## Brand Constraints

- 홍승현 pages must stay focused on international-school Physics, easy understanding, AP/GPA/exam application, and confidence. Do not reintroduce Art/Business/Finance/Economics/Media expansion messaging unless the user explicitly asks.
- 엘리쌤 pages focus on English / Academic English, GPA/AP/SAT/TOEFL, easy explanation, time efficiency, and student-paced curriculum.
- 세현 pages focus on platform planning, international-school consulting context, lightboard-based visual explanation, structured application, and trust.

