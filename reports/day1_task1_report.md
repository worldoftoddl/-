## 작업 요약

- 디렉토리 생성 완료: `docs`, `sources`, `reviews`, `reports`
- Chapter 2 작성 완료: `docs/02_agentic_ai_concept.md`
- 본문은 생성형 AI와 에이전틱 AI의 차이, 4대 특성, LangGraph·AutoGen·CrewAI 비교, 본 보고서의 분석 명제를 포함함.
- Gartner 보조 후보는 `web.open`으로 내용 확인은 가능했으나 `curl` HTTP 검증에서 403을 반환하여 본문 사용 출처에서는 제외함.

## Self-Check 결과

| 항목 | 결과 | 근거 |
|---|---:|---|
| 1. `wc -m` 1,350~1,650자 | PASS | `1577 docs/02_agentic_ai_concept.md` |
| 2. 4대 특성 및 예시 | PASS | 계획, 도구사용, 다단계실행, 자율성 각각 등장. 각 항목 뒤에 계약서 검토, 회계 자료 조회, 판례 재검색, API 재시도 예시 포함 |
| 3. 프레임워크 3종 비교 | PASS | LangGraph, AutoGen, CrewAI 각각 강점·약점·대표 사용처 기술 |
| 4. 금지 표현 grep 0건 | PASS | `rg` 결과 출력 없음 |
| 5. 시점 표기 | PASS | 1문단 첫 문장에 `2026년 5월 기준` 표기 |
| 6. 사용 출처 URL 접근 가능 | PASS | 본문 사용 URL 6개 모두 HTTP 200 |

## Paraphrase 매핑

| 원문 표현 | 재구성 표현 | 처리 이유 |
|---|---|---|
| "autonomous, task-oriented AI agents" | 목표를 입력받은 뒤 절차를 나누고 다음 행동을 조정하는 실행 체계 | 자율성을 과장하지 않고 업무 흐름 관점으로 재정의 |
| "LLMs using tools based on environmental feedback in a loop" | 관찰과 수정의 반복으로 과업을 끝내는 다단계 실행 | 루프 구조를 한국어 분석 문장으로 재구성 |
| "tool calls" | 검색, 데이터베이스, 업무 소프트웨어, 코드 실행기를 호출 | 추상 용어를 전문서비스 업무 예시로 구체화 |
| "low-level orchestration framework and runtime" | 상태 보존, 중단, 사람 승인, 장기 실행에 강한 프레임워크 | LangGraph의 기능을 보고서 목적에 맞게 요약 |

## 사용 출처 URL 목록 + 접근 검증 결과

| 출처 | URL | 검증 |
|---|---|---:|
| a16z | https://a16z.com/the-rise-of-computer-use-and-agentic-coworkers/ | HTTP 200 |
| Anthropic | https://www.anthropic.com/engineering/building-effective-agents | HTTP 200 |
| LangChain State of AI 2024 | https://www.langchain.com/blog/langchain-state-of-ai-2024 | HTTP 200 |
| LangGraph docs | https://docs.langchain.com/oss/python/langgraph/overview | HTTP 200 |
| Microsoft Research AutoGen | https://www.microsoft.com/en-us/research/project/autogen/ | HTTP 200 |
| CrewAI docs | https://docs.crewai.com/en/introduction | HTTP 200 |

## 클리셰 grep 명령과 결과

명령:

```bash
rg -n '<금지 표현 6종 정규식>' docs/02_agentic_ai_concept.md
```

결과:

```text
출력 없음. exit code 1은 매칭 0건을 의미함.
```

## AGENTS.md Per-Task Self-Check

| 항목 | 결과 | 근거 |
|---|---:|---|
| 분량 명세 충족 | PASS | 1,577자 |
| 클리셰 없음 | PASS | 금지 표현 0건 |
| 모든 사실 출처 명시 | PASS | 본문 각주 1~4 |
| 패러프레이즈 처리 | PASS | 원문 구조를 한국어 분석 문장으로 재구성 |
| 한국어 학술 톤 일관 | PASS | `~이다`, `~로 본다`, `~된다` 중심 |
| 시점 명시 | PASS | 1문단 표기 |
| 출처 URL 접근 가능 | PASS | 사용 URL 6개 HTTP 200 |
