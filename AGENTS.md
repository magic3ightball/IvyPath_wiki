# IvyPath LLM Wiki Agent Guide

This folder is a Karpathy style LLM Wiki for IvyPath.

## Source of truth

Raw source files live in `raw/`. Treat them as the source of truth. Do not rewrite raw files unless the user explicitly asks to correct or replace the original source.

Compiled wiki pages live in `people/`, `brand/`, `students/`, `curriculum/`, `content/`, `sales`, and `sources/`. These pages may be updated by agents when new raw source material changes the wiki.

`_index.md` is the navigation layer. Keep it current when adding, deleting, renaming, or materially changing pages.

`_log.md` is the maintenance history. Add a short dated entry after ingest, restructuring, or policy changes.

## Workflow

1. Read `_index.md` first to understand the current map.
2. Read `rules/위키 운영 규칙.md` before editing wiki pages.
3. For factual edits, inspect the linked `raw/` or `sources/` material first.
4. Update only the pages affected by the source material or the user request.
5. Preserve Obsidian wikilinks and frontmatter.
6. Do not invent new brand claims, credentials, results, or positioning that are not supported by existing source material.
7. When a new source is added, place it in `raw/`, create or update a `sources/` summary, then update affected compiled pages.
8. Keep the repo clean enough for Obsidian Git to auto sync to `magic3ightball/IvyPath_wiki`.

## Folder roles

`raw/` stores original input material.

`sources/` stores structured summaries of raw material.

`people/` stores person level memory.

`brand/` stores brand positioning, values, and promise.

`students/` stores target student personas and pain points.

`curriculum/` stores course and exam positioning.

`content/` stores teaching method and learning experience.

`sales/` stores parent persuasion, detail page copy, and sales messages.

## Current branding guardrail

For 홍승현 Physics branding, do not use the excluded framing that Physics is a language for Economics, Business, Art, Finance, or the AI era. Do not use the excluded framing that the brand helps students imagine a bigger future. The current main branding is: 양치기 없이 적은 문제로 깊게 이해시키는 Physics.
