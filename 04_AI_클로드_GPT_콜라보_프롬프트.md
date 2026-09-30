# 프롬프트 — 04_AI_클로드_GPT_콜라보.html 재현용

다른 세션에 아래 [프롬프트 본문]을 그대로 붙여넣으면 동일한 산출물을 얻을 수 있다.

## 전제 조건

- 작업폴더 `260920_AI`를 연결한 상태에서 실행
- 입력 파일 없음 (내용은 프롬프트 본문에 포함)
- 사용 스킬: 없음 (단일 HTML 파일 직접 작성). 프로젝트 목록은 WebSearch로 GitHub 검색 후 정리한 것

## 프롬프트 본문

```
04_AI_클로드_GPT_콜라보.html 파일을 새로 만들어서 아래의 내용으로 만들고, index.html에 4번째 항목으로 추가해줘.
일반 PC 화면에서 보는 용도로 구성할 것. [자동판단]

[표현할 내용]
- 주제: Claude가 결과물을 만들고 → GPT가 검토해 미비사항을 작성하고 → Claude가 처리하고 → 반복.
  사용자 의사결정이 필요한 부분만 제외하고 자동 처리. API 과금 없이 구독 계정만으로 돌리는 방법.
- 1. 생성자·검토자 루프 구조: 사용자 명령 1회 → Claude 결과물 v1 → GPT 검토(JSON: approved / needs_user_decision / needs_work)
  → Claude 수정 → 최대 N회 반복. 검토 결과 JSON 형식 예시 포함.
- 2. API 대신 CLI: Claude Code(Claude Pro/Max 구독, `claude -p`) ↔ Codex CLI(ChatGPT Plus/Pro 구독, `codex login`, `codex exec`) 비교표.
  Claude Code 세션 안에서 Bash로 codex exec를 리뷰어처럼 호출하는 구성 설명.
- 3. GitHub 공개 프로젝트 6개:
  hamelsmu/claude-review-loop (★723, Stop 훅, Codex 리뷰어 최대 4개 병렬),
  promptadvisers/claudex (기획/설계, PLAN.md, 라운드마다 다른 관점, --rounds N),
  wwind123/coding-review-agent-loop (Python 오케스트레이터, 구독 CLI 사용 컨셉),
  Mauritiusllewelynpowys919/codex-review (멀티 라운드 추적),
  adamjgmiller/adamsreview (리뷰어 선택형),
  flowmar47/clodex-loop (역방향: Codex 개발·Claude 검토).
  참고 글: https://smartscope.blog/en/blog/claude-code-codex-review-loop-automation-2026/
- 4. 공통 동작 원리 4단계.
- 5. 추천 및 설치: 코드 → claude-review-loop (설치 명령 2줄), 기획서 → claudex. 사전 준비 명령(codex --version / npm i -g @openai/codex / codex login).
- 6. 주의: 구독 사용량 한도(5시간 창), 하면 안 되는 것(브라우저 자동화·토큰 추출 = 약관 위반), 설계 시 정할 것(종료 조건·검토 기준·사용자 결정 분리·결과물 종류).

[구성] [자동판단]
1. 페이지 제목: "AI 클로드 × GPT 콜라보", 상단에 "API 과금 없음" 배지
2. 섹션 6개를 세로로 배치한 카드, 섹션 제목은 색상 배지
3. 1번 섹션의 흐름은 역할(사용자/Claude/GPT/제어) 아이콘이 붙은 단계 목록
4. 3번 섹션은 프로젝트 카드 2열 그리드, 추천 2개는 테두리 강조, GitHub 링크는 새 탭
5. 5·6번 섹션은 2단 박스

[출력 규칙]
- 같은 폴더의 03_AI활용_툴.html, index.html과 같은 디자인 톤(색 변수, 카드, 맑은 고딕) 유지 [자동판단]
- 최대 폭 1200px, 860px 미만에서는 1열로 전환 [자동판단]
- 라이트/다크 모드 지원, 외부 라이브러리·폰트 없는 단일 HTML [자동판단]
- 파일 형식: html
- 파일명: 04_AI_클로드_GPT_콜라보.html
- 저장 위치: 이 프롬프트 파일과 같은 폴더 (작업폴더 루트)
- index.html: 4번째 항목 추가(보라색 --c4 변수 추가), 하단 "페이지 4개"로 수정, 프롬프트 링크는 04_AI_클로드_GPT_콜라보_프롬프트.md
```

> `[자동판단]`이 붙은 줄은 원 요청자가 지시한 것이 아니라 재현을 위해 채워 넣은 조건이다.
> 바꿔도 무방하다. 표식이 없는 줄이 실제 요구사항이다.

## 재현 시 참고사항

- 원 요청일: 2026-09-20
- 생성 파일: `04_AI_클로드_GPT_콜라보.html`, `04_AI_클로드_GPT_콜라보_프롬프트.md`, `index.html` 수정
- 내용은 같은 세션에서 나눈 대화(SQLite vs PostgreSQL → Claude×GPT 루프 → 구독 기반 → GitHub 프로젝트 검색)의 마지막 답변을 정리한 것
- 프로젝트 별점(★723)은 2026-09-20 검색 시점 기준
