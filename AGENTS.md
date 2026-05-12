# AGENTS.md

## Project: 졸업 트렌드 리포트
**전문 지식서비스 산업(회계·법무·컨설팅)의 Agentic AI 도입 양상 비교 분석**

---

## Hard Constraints

| 항목 | 값 |
|---|---|
| 분량 | A4 15매 이상 (표지·목차·참고문헌 제외) |
| 언어 | 한국어 |
| 최종 포맷 | 한글(HWP) — 본인이 직접 변환, Codex는 마크다운까지만 |
| Turnitin 유사도 | 7% 이하 (필수) |
| KCI 유사도 검사 | 통과 |
| 마감 | 2026-05-17 (일) |
| 현재 시점 | 2026-05-12 (화) |
| 시점 명시 | "2026년 5월 기준" 본문 초반에 박을 것 |

---

## Output Directory Structure

```
/docs              # 본문 챕터
  01_intro.md
  02_agentic_ai_concept.md
  03_accounting.md
  04_legal.md
  05_consulting.md
  06_comparative_skeleton.md      # Day 1
  06_comparative_matrix.md        # Day 3
  06_comparative_full.md          # Day 4
  07_implications.md
  08_conclusion.md
  full_draft_v1.md                # Day 4 통합
  full_draft_v2.md                # Day 5 패러프레이즈 후
  final_report.md                 # Day 5 최종
  references.md
/sources           # 자료 매트릭스
  source_matrix_accounting.md
  source_matrix_legal.md
  source_matrix_consulting.md
/reviews           # 검토 노트
  devils_advocate_review.md
  paraphrase_log.md
/reports           # 일별 진행 보고서
  day{N}_report.md
```

---

## Locked Configuration (변경 금지)

### 5대 비교 변수
1. **규제 강도** — 업무 결과물에 대한 외부 규제 강도
2. **책임 소재** — 잘못된 결과물에 대한 법적 책임 무게
3. **업무 정형성** — 정형화·반복 가능성 vs 맥락 의존 판단
4. **고객 구조** — 단일 거대 고객 vs 다수 고객 구조
5. **자격·진입장벽** — 면허 체계와 AI 활용 제한

### 챕터 구성 및 분량 (총 16매)
| Ch | 제목 | 분량 |
|---|---|---|
| 1 | 서론 | 1.5매 |
| 2 | Agentic AI 개념 정리 | 1.5매 |
| 3 | 회계 산업 도입 양상 | 3매 |
| 4 | 법무 산업 도입 양상 | 3매 |
| 5 | 컨설팅 산업 도입 양상 | 2.5매 |
| 6 | 비교 분석 (핵심) | 3매 |
| 7 | 시사점 | 1매 |
| 8 | 결론 | 0.5매 |

**1매 ≈ 1,000자** (한글 기본 설정 기준)

---

## Writing Style Guide

### 톤
- 한국 학술 보고서 톤 (~이다, ~로 나타난다, ~를 시사한다)
- 능동태 우선, 패시브 절제
- 1문장 평균 40~60자
- 단락당 3~6문장

### 용어
- 전문 용어 첫 등장 시 영문 병기: *거대언어모델(Large Language Model, LLM)*
- 외래어는 한국어 음차 우선, 필요시 원어 병기
- "AI 에이전트", "에이전틱 AI" 혼용 가능 (Agentic AI 개념 첫 등장 시 정의)

### 시점
- 본 보고서는 "2026년 5월 기준"으로 작성됨을 1장 또는 2장 초반에 명시
- 사례 발표일은 모두 "YYYY-MM" 형식으로 통일

---

## Prohibited Practices

### 표현 금지
- 클리셰: "AI 혁명", "패러다임 시프트", "게임 체인저", "우리 삶을 바꾸고 있다", "더 이상 무시할 수 없는", "필연적 흐름"
- 결론 미리 정해놓고 사례 끼워 맞추기
- 저자 편향 노출: CPA 지망자가 CPA 직업의 우월성을 방어하는 논조

### 인용 금지
- 자료 원문 표현 15어 이상 직접 차용
- 한 출처에서 직접 인용 2회 이상
- 출처 없는 수치·통계

---

## Citation Rules

- **직접 인용**: 15어 이하만 큰따옴표 + 각주 번호
- **패러프레이즈**: 본인 표현으로 재구성 + 각주 번호
- **각주 양식**: Chicago 17th (학과 양식 미확정 시 기본값)
- 모든 수치·날짜·고유명사는 출처 명시
- 추정치는 "추정", "약" 등으로 표시

---

## Source Priority Lists

### 회계 (우선순위 순)
1. EY.ai 공식 발표 (2023-09)
2. KPMG Clara 공식 페이지
3. PwC ChatPwC / 삼일 AX Node (채용공고, 임원 인터뷰)
4. Deloitte Omnia DNAV
5. 한국공인회계사회 *공인회계사 미래 대응* 보고서
6. 삼정KPMG 경제연구원 *생성형 AI* 시리즈
7. *Accounting Today*, *Journal of Accountancy*

### 법무 (우선순위 순)
1. Harvey AI 공식 블로그 + Sequoia Capital 투자 라운드 발표
2. Allen & Overy + Harvey 파트너십 발표 (2023-02)
3. Casetext CoCounsel + Thomson Reuters 인수 (2023-06)
4. Stanford CodeX 리포트
5. Thomson Reuters *Future of Professionals Report 2024/2025*
6. 대한변호사협회 *리걸테크 백서* (존재 시)
7. Law&Company, LBox 보도자료

### 컨설팅 (우선순위 순)
1. McKinsey Lilli 공식 발표 (2023-08) + 후속 사용 통계
2. BCG-X / GENE 공식 자료
3. Bain.ai (OpenAI 협업 발표)
4. Accenture AI Refinery
5. Source Global Research 컨설팅 산업 보고서
6. *The Information*, *Financial Times* 컨설팅 섹션

### Agentic AI 정의 (Ch.2 전용)
1. Andreessen Horowitz, *"The State of Agentic AI"* (a16z.com)
2. Anthropic, *"Building effective agents"* (engineering blog)
3. LangChain, *"State of AI Agents 2024"*
4. Gartner *Hype Cycle for AI 2025*

---

## Plagiarism Risk Zones (Day 5 패러프레이즈 우선순위)

1. **Agentic AI 정의** — a16z, Anthropic 자료는 반드시 본인 어휘로 재구성
2. **빅4 보도자료 표현** — 모두 패러프레이즈, 직접 표현 차용 금지
3. **클리셰 표현** — 본인 표현으로 대체
4. **학술 자료 15어 이상 표현** — 분량 축소 또는 패러프레이즈

---

## Per-Task Self-Check (모든 task 종료 시)

각 task 결과물에 대해 self-check 수행 후 보고:
- [ ] 분량 명세 충족? (±10%)
- [ ] 클리셰 없음?
- [ ] 모든 사실 출처 명시?
- [ ] 패러프레이즈 처리?
- [ ] 한국어 학술 톤 일관?
- [ ] 시점 명시?
- [ ] 출처 URL 접근 가능?

---

## Tool Usage

- `web_search`, `web_fetch`: 자료 수집 task에서 적극 활용
- `shell` / 파일 시스템: 디렉토리 구조 생성, 파일 통합
- 인터넷 접근 시 1차 자료 우선, 위키피디아·블로그 보조 자료만

---

## Hand-off Points (본인 직접 작업, Codex 위임 불가)

| 시점 | 작업 |
|---|---|
| Day 5 오후 | 마크다운 → HWP 변환 |
| Day 5 오후 | 학과 양식 적용 (폰트·줄간격·여백·표지·목차) |
| Day 5 오후 | Turnitin 사전 검사 |
| Day 6 (일) 오전 | 최종 검토 및 제출 |
