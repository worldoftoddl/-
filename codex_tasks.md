# Codex Tasks
## 졸업 트렌드 리포트 5일 작업 - Task별 실행 프롬프트

---

## 사용 방법

1. **AGENTS.md를 프로젝트 루트에 커밋** — Codex가 모든 task 시작 시 자동으로 로드합니다.
2. 아래 task를 **하나씩 복사하여 Codex task input에 붙여넣기**.
3. **병렬 표시** 된 task는 Codex 대시보드에서 동시 launch 가능.
4. Codex는 task 간 메모리가 없으므로, 각 task는 자체적으로 필요한 파일을 `Required Reading`에서 읽어야 함.
5. 각 task 완료 후 산출물 확인 후 다음 task 진행.

---

# DAY 1 (화 5/12 저녁)

## Task 1.1: 프로젝트 초기화 + Chapter 2 작성

```
[Role]
한국어 학술 보고서 작성 전문가. AI 기술에 대한 정확한 이해를 보유.

[Required Reading]
- AGENTS.md (프로젝트 루트)

[Task]
1. 디렉토리 구조 생성:
   - /docs, /sources, /reviews, /reports
2. Chapter 2 (Agentic AI 개념 정리) 본문 작성
   - 출력 파일: /docs/02_agentic_ai_concept.md
   - 분량: 1.5매 (1,350~1,650자)

[Content Structure - Chapter 2]
단락 1 (~300자): 생성형 AI vs Agentic AI 명확한 구분
단락 2 (~500자): Agentic AI 4대 특성 — 계획(Planning) / 도구사용(Tool Use) / 다단계실행(Multi-step Execution) / 자율성(Autonomy). 각 특성에 1줄 예시.
단락 3 (~400자): 주요 프레임워크 3종 — LangGraph, AutoGen, CrewAI 비교
단락 4 (~250자): 본 보고서의 분석 다리 — "Agentic AI는 단일 모델이 아니라 모델·도구·메모리·계획 모듈의 결합체이며, 이 결합 방식이 산업 도입의 변수가 된다"는 명제로 연결

[Sources]
AGENTS.md §Source Priority §Agentic AI 정의 — web_search 활용:
- a16z.com "Agentic AI"
- Anthropic "Building effective agents"
- LangChain "State of AI Agents"

[Constraints]
- 직접 인용 15어 이하, 각주 번호 표시
- a16z·Anthropic 정의는 본인 표현으로 재구성 (Plagiarism Risk Zone 1순위)
- 클리셰 금지
- "2026년 5월 기준" 본문에 명시

[Output Validation]
- 글자 수 1,350~1,650
- 4대 특성 모두 포함
- 프레임워크 3종 비교 단락 존재
- AGENTS.md §Per-Task Self-Check 모두 충족

[Output Files]
- /docs/02_agentic_ai_concept.md
- /reports/day1_task1_report.md (작업 요약 + self-check 결과)
```

---

## Task 1.2: Chapter 6 골격 작성

```
[Role]
비교 분석 프레임워크 설계 전문가.

[Required Reading]
- AGENTS.md §Locked Configuration §5대 비교 변수

[Task]
Chapter 6 (비교 분석) 골격 문서 작성. 본문은 Day 3-4에 채움.

[Output File]
/docs/06_comparative_skeleton.md

[Content Structure]
## 1. 도입부 (~200자)
비교 프레임워크 소개. 왜 5대 변수가 적절한가.

## 2. 5대 변수 정의 (각 100~150자)
### 2.1 규제 강도
정의: 업무 결과물에 대한 외부 규제 강도 (금융감독원, 대한변협, 자율 등)
측정: 면허 박탈·인증 취소 가능 여부, 외부 감독 빈도

### 2.2 책임 소재
정의: 잘못된 결과물에 대한 법적 책임 무게
측정: 소송 가능성, 손해배상 범위, 면허 책임

### 2.3 업무 정형성
정의: 정형화·반복 가능성 vs 맥락 의존 판단
측정: 표준 절차 비중, 정답 vs 판단 영역

### 2.4 고객 구조
정의: 단일 거대 고객 vs 다수 고객
측정: 매출 집중도, 고객 유형 분포

### 2.5 자격·진입장벽
정의: 면허 체계와 AI 활용 제한
측정: 면허 요건, AI 도구 사용에 대한 규정

## 3. 빈 매트릭스 (Day 3에 채움)
| 변수 | 회계 | 법무 | 컨설팅 |
|---|---|---|---|
| 규제 강도 | [TBD] | [TBD] | [TBD] |
| 책임 소재 | [TBD] | [TBD] | [TBD] |
| 업무 정형성 | [TBD] | [TBD] | [TBD] |
| 고객 구조 | [TBD] | [TBD] | [TBD] |
| 자격·진입장벽 | [TBD] | [TBD] | [TBD] |

## 4. 작업 가설 (Day 3-4에 사례로 검증)
"규제·책임이 약하고 정형성이 낮은 컨설팅이 가장 공격적으로 도입.
회계는 정형 영역부터 도입하되 감사 핵심 판단은 보류.
법무는 책임소재 무게로 가장 신중."

[Constraints]
- 변수 정의는 학술 톤, 측정 방법 명시
- 가설은 사례 검증 대상 (결론 아님)
- 분량 무관 (골격이므로)

[Output Validation]
- 5대 변수 정의·측정 방법 모두 명시
- 빈 매트릭스 표 존재
- 가설 명시

[Output Files]
- /docs/06_comparative_skeleton.md
- /reports/day1_task2_report.md
```

---

# DAY 2 (수 5/13) — 병렬 실행

## Task 2.1, 2.2, 2.3 동시 launch 가능

---

## Task 2.1: 회계 산업 자료 수집

```
[Role]
산업 리서치 분석가. 1차 자료 수집에 집중.

[Required Reading]
- AGENTS.md (전체)
- /docs/06_comparative_skeleton.md (5대 변수 정의)

[Task]
회계 산업의 Agentic AI / 생성형 AI 도입 사례를 수집하여 매트릭스 작성.

[Output File]
/sources/source_matrix_accounting.md

[Source Priority]
AGENTS.md §Source Priority §회계 우선순위 따름:
1. EY.ai (2023-09)
2. KPMG Clara
3. PwC ChatPwC / 삼일 AX Node
4. Deloitte Omnia DNAV
5. 한국공인회계사회 보고서
6. 삼정KPMG 경제연구원

[Output Format]
## 사례 매트릭스
| # | 사례명 | 제공사 | 출시일 | 도입 영역 | 시장 | 출처 URL |
|---|---|---|---|---|---|---|
| 1 | EY.ai | EY | 2023-09 | 감사/세무/자문 | 글로벌 | <URL> |
| ... |

## 사례별 상세
### 사례 N: <사례명>
- 출처: <URL>
- 핵심 기능: ...
- 도입 영역: ...
- 발표 시 강조점: ...
- 핵심 인용구 (원문, 15어 이하):
  > "..."
- 한국어 패러프레이즈: ...
- 5대 변수 매핑 (Ch.6 활용용):
  - 규제 강도: <이 사례가 규제 강도에 대해 시사하는 바>
  - 책임 소재: ...
  - 업무 정형성: ...
  - 고객 구조: ...
  - 자격·진입장벽: ...
- 한계·반론: <이 사례의 약점, 과장된 부분>

[Constraints]
- 사례 수 5~7개 (강제 캡, 절대 초과 금지)
- 1차 자료 80% 이상 (공식 보도자료, 임원 인터뷰, 자체 발표)
- 위키피디아·블로그는 보조 자료로만
- 모든 URL 접근 가능 확인 (web_fetch로 검증)
- 핵심 인용구 15어 이하

[Tools]
web_search, web_fetch 적극 활용.

[Output Validation]
- 사례 5~7개
- 모든 URL 검증됨
- 모든 사례에 5대 변수 매핑 완료
- 한계·반론 단락 모두 작성

[Output Files]
- /sources/source_matrix_accounting.md
- /reports/day2_task1_report.md
```

---

## Task 2.2: 법무 산업 자료 수집

```
[Role]
산업 리서치 분석가.

[Required Reading]
- AGENTS.md (전체)
- /docs/06_comparative_skeleton.md

[Task]
법무 산업의 Agentic AI / 생성형 AI 도입 사례 매트릭스 작성.

[Output File]
/sources/source_matrix_legal.md

[Source Priority]
AGENTS.md §Source Priority §법무 우선순위 따름.

[Output Format]
Task 2.1과 동일 (사례 매트릭스 + 사례별 상세 + 5대 변수 매핑 + 한계·반론).

[Special Note - 한국 시장 처리]
한국 법무 자료가 영미권보다 빈약함은 *분석 대상*임.
- 한국 사례 부족을 분석 매트릭스의 "분석 가능 부분"으로 명시
- 별도 단락 "한국 법무 시장의 미성숙도"에 다음 요인 기록:
  · 변호사법 제한
  · 로톡 사태 (2022~2023)
  · 대한변협의 리걸테크 보수성
  · 시장 규모와 투자 부재

[Constraints]
- 사례 수 5~7개
- 영미권 중심이되 한국 사례 최소 1~2개 포함
- 1차 자료 80% 이상

[Output Files]
- /sources/source_matrix_legal.md
- /reports/day2_task2_report.md
```

---

## Task 2.3: 컨설팅 산업 자료 수집

```
[Role]
산업 리서치 분석가.

[Required Reading]
- AGENTS.md (전체)
- /docs/06_comparative_skeleton.md

[Task]
컨설팅 산업의 Agentic AI / 생성형 AI 도입 사례 매트릭스 작성.

[Scope Definition]
컨설팅 = MBB (McKinsey, BCG, Bain) + Accenture
빅4 자문본부는 본 챕터 제외 (Chapter 3 회계에서 다룸)

[Output File]
/sources/source_matrix_consulting.md

[Source Priority]
AGENTS.md §Source Priority §컨설팅 우선순위 따름.

[Output Format]
Task 2.1과 동일.

[Constraints]
- 사례 수 5~7개
- 글로벌 중심 (한국 컨설팅 시장 자료 빈약 — 영미권 중심)
- 1차 자료 80% 이상

[Output Files]
- /sources/source_matrix_consulting.md
- /reports/day2_task3_report.md
```

---

# DAY 3 (목 5/14)

## Task 3.1, 3.2, 3.3 병렬 실행 가능 (자료 매트릭스 완성 후)

---

## Task 3.1: Chapter 3 (회계) 본문 작성

```
[Role]
한국어 학술 보고서 작성 전문가 + 회계 도메인 지식 보조자.
(주의: 회계 도메인 최종 책임은 본인. 본 task는 보조.)

[Required Reading]
- AGENTS.md
- /sources/source_matrix_accounting.md (모든 사례 활용)
- /docs/06_comparative_skeleton.md (5대 변수)

[Task]
Chapter 3 (회계 산업의 Agentic AI 도입 양상) 본문 작성.

[Output File]
/docs/03_accounting.md

[Content Structure]
## 3.1 회계 산업 개관 (~300자)
회계법인의 3대 본부 구조 (감사·세무·자문)와 각 본부의 업무 성격 차이.

## 3.2 글로벌 빅4의 Agentic AI 도입 (~1,200자)
- EY.ai (2023-09 출시): 핵심 기능, 도입 영역
- KPMG Clara: 강점, 차별화
- Deloitte Omnia DNAV: 감사 자동화 초점
- PwC ChatPwC: 활용 범위
각 사례에 5대 변수 중 관련 변수 자연스럽게 언급.

## 3.3 한국 빅4의 대응 (~1,000자)
- 삼일 AX Node 중심 분석 (조직 구조, 채용 현황)
- 한영(EY)·안진(딜로이트)·삼정(KPMG) 간략 비교
- 글로벌 본사 전략과 한국 법인의 격차

## 3.4 도입 영역별 진단 (~500자)
- 감사 영역: 어디까지 도입, 어디부터 보류
- 세무 영역: 자동화 진척
- 자문 영역: 가장 공격적 도입

[Constraints]
- 분량 3매 ± 10% (2,700~3,300자)
- /sources/source_matrix_accounting.md의 사례만 사용 (외부 사례 추가 금지)
- 직접 인용은 사례당 최대 1회, 15어 이하
- 각주 번호로 모든 사실 출처 표시
- "2026년 5월 기준" 시점 명시
- 클리셰 금지

[Output Validation]
- 글자 수 2,700~3,300
- 매트릭스의 회계 사례 모두 본문 등장
- 5대 변수 중 최소 3개 자연스럽게 언급
- 각주 번호 정상

[Output Files]
- /docs/03_accounting.md
- /reports/day3_task1_report.md
```

---

## Task 3.2: Chapter 4 (법무) 본문 작성

```
[Role]
한국어 학술 보고서 작성 전문가.

[Required Reading]
- AGENTS.md
- /sources/source_matrix_legal.md
- /docs/06_comparative_skeleton.md

[Task]
Chapter 4 (법무 산업의 Agentic AI 도입 양상) 본문 작성.

[Output File]
/docs/04_legal.md

[Content Structure]
## 4.1 법무 산업 개관 (~250자)
대형 로펌과 리걸테크 시장의 분리, 변호사 자격제도의 특수성.

## 4.2 Harvey AI 사례 심층 분석 (~900자)
- 출시 배경, 핵심 기능
- Allen & Overy 파트너십 (2023-02): 초기 도입 사례
- 후속 확장 (PwC 등)
- 5대 변수 중 책임 소재·자격 변수와의 연관

## 4.3 인접 사례 (~600자)
- Casetext CoCounsel + Thomson Reuters 인수 (2023-06)
- 기타 글로벌 리걸테크

## 4.4 한국 법무 시장의 미성숙도 (~700자)
영미권 대비 한국 시장의 도입 지연 원인 분석:
- 변호사법 제한
- 로톡 사태 (2022~2023)
- 대한변협의 리걸테크 보수성
- 한국 리걸테크 (Law&Company, LBox 등) 현황

## 4.5 소결 (~250자)
법무 산업 도입의 구조적 특징 요약.

[Constraints]
- 분량 3매 ± 10%
- /sources/source_matrix_legal.md 사례만 사용
- 직접 인용은 사례당 최대 1회, 15어 이하

[Output Files]
- /docs/04_legal.md
- /reports/day3_task2_report.md
```

---

## Task 3.3: Chapter 5 (컨설팅) 본문 작성

```
[Role]
한국어 학술 보고서 작성 전문가.

[Required Reading]
- AGENTS.md
- /sources/source_matrix_consulting.md
- /docs/06_comparative_skeleton.md

[Task]
Chapter 5 (컨설팅 산업의 Agentic AI 도입 양상) 본문 작성.

[Output File]
/docs/05_consulting.md

[Content Structure]
## 5.1 컨설팅 산업 개관 (~250자)
MBB + Accenture 중심. 규제·자격이 약한 시장 특성.

## 5.2 McKinsey Lilli 사례 (~700자)
- 2023-08 출시 배경
- 활용 범위 (45,000명 직원, 70% 활용)
- 도입 후 매출 영향

## 5.3 BCG-X / GENE (~500자)
- BCG의 AI 전담 조직
- GENE 플랫폼 특징

## 5.4 Bain.ai + Accenture (~500자)
- Bain의 OpenAI 협업
- Accenture AI Refinery

## 5.5 컨설팅 산업의 도입 패턴 (~550자)
- 가장 공격적 도입 양상의 구조적 원인
- 5대 변수와의 직접 연관 (규제 약함, 책임 자유로움)

[Constraints]
- 분량 2.5매 ± 10% (2,250~2,750자)
- /sources/source_matrix_consulting.md 사례만 사용

[Output Files]
- /docs/05_consulting.md
- /reports/day3_task3_report.md
```

---

## Task 3.4: Chapter 6 매트릭스 채우기 (Day 3 후반, 3.1~3.3 완료 후)

```
[Role]
비교 분석 전문가.

[Required Reading]
- /sources/source_matrix_accounting.md
- /sources/source_matrix_legal.md
- /sources/source_matrix_consulting.md
- /docs/06_comparative_skeleton.md
- /docs/03_accounting.md, /docs/04_legal.md, /docs/05_consulting.md

[Task]
5대 변수 × 3개 산업 매트릭스의 모든 셀(15개)을 사례 기반으로 채우십시오.

[Output File]
/docs/06_comparative_matrix.md

[Content Structure]
## 1. 매트릭스 (15셀 모두 채움)
| 변수 | 회계 | 법무 | 컨설팅 |
|---|---|---|---|
| 규제 강도 | <진단> [사례 #N] | <진단> [사례 #M] | <진단> [사례 #K] |
| ... |

각 셀: 짧은 진단 (50~80자) + 근거 사례 번호.

## 2. 변수별 비교 분석 (5개 단락 × 각 200~250자)
### 2.1 규제 강도 비교
3개 산업의 규제 강도 차이를 사례로 설명. 차이의 구조적 원인.
(이하 2.2~2.5 동일 구조)

## 3. 가설 검증 결과 (~500자)
Day 1 가설 ("컨설팅이 가장 공격적, 법무가 가장 신중") 이 사례에 의해 어떻게 지지/수정되었는가.
- 지지된 부분
- 수정 필요한 부분
- 가설을 넘어선 발견

[Constraints]
- 모든 진단에 매트릭스 사례 번호 인용
- 차이가 없는 변수가 있다면 정직하게 명시
- 가설 검증 결과를 사례 자체에서 도출

[Output Validation]
- 15셀 모두 채워짐 (TBD 잔존 금지)
- 변수별 단락 5개 모두 존재
- 가설 검증 명확

[Output Files]
- /docs/06_comparative_matrix.md
- /reports/day3_task4_report.md
```

---

# DAY 4 (금 5/15)

## Task 4.1: Chapter 6 본문 완성

```
[Role]
한국어 학술 보고서 작성 전문가.

[Required Reading]
- AGENTS.md
- /docs/06_comparative_matrix.md
- /docs/06_comparative_skeleton.md
- /docs/03_accounting.md, /docs/04_legal.md, /docs/05_consulting.md

[Task]
Chapter 6 본문 완성. 매트릭스를 서사화하여 학술 보고서 톤으로.

[Output File]
/docs/06_comparative_full.md

[Content Structure]
## 6.1 비교 프레임워크 (~300자)
도입부. 왜 5대 변수인가, 어떻게 사용하는가.

## 6.2 변수별 비교 분석 (5개 × 각 ~500자, 총 2,500자)
### 6.2.1 규제 강도 — 회계·법무 vs 컨설팅
사례 기반 비교, 차이의 구조적 원인.
(이하 6.2.2~6.2.5 동일 구조)

## 6.3 5대 변수가 만드는 도입 속도의 격차 (~500자)
변수가 어떻게 결합되어 도입 속도 격차로 이어지는가.

## 6.4 가설 검증 결과 (~300자)
Day 1 가설이 어떻게 지지/수정되었는가.

[Constraints]
- 분량 3매 ± 10% (2,700~3,300자)
- 매트릭스 데이터를 단순 나열하지 말고 서사 구성
- 각 단락에 최소 1개 사례 인용
- 직접 인용 사례당 최대 1회, 15어 이하
- 각주 번호 정상
- 클리셰 금지

[Output Validation]
- 글자 수 2,700~3,300
- 5대 변수 모두 별도 단락
- 사례 매트릭스의 사례 모두 활용
- 가설 검증 명확

[Output Files]
- /docs/06_comparative_full.md
- /reports/day4_task1_report.md
```

---

## Task 4.2: Chapter 1·7·8 작성 (서론·시사점·결론)

```
[Role]
한국어 학술 보고서 작성 전문가.

[Required Reading]
- AGENTS.md
- /docs/ 폴더의 02~06 챕터 (본문 완성된 상태)

[Task]
Chapter 1 (서론), Chapter 7 (시사점), Chapter 8 (결론) 작성.
서론은 본문 완성 후 쓰는 것이 정확함.

[Output Files]
- /docs/01_intro.md (1.5매, ~1,500자)
- /docs/07_implications.md (1매, ~1,000자)
- /docs/08_conclusion.md (0.5매, ~500자)

[Chapter 1 Structure]
1. 문제의식 (~400자): 2026년 시점에서 왜 이 비교가 중요한가
2. 연구 대상·범위 (~300자): 3개 산업, Agentic AI 정의, 시점
3. 연구 방법 (~300자): 사례 비교 분석, 5대 변수, 1차 자료 중심
4. 보고서 구성 (~250자): 각 챕터 간략 소개
5. 보고서 한계 (~250자): 자료 비대칭, 시점 제약 정직 명시

[Chapter 7 Structure]
1. 한국 전문서비스 산업의 함의 (~400자):
   - 한국 회계법인 AX 전략 방향
   - 한국 리걸테크 시장 발전 가능성
   - 한국 컨설팅의 글로벌 격차
2. 향후 5년 전망 (~400자):
   - 도입 속도 격차의 수렴/확대 가능성
   - 신규 직업 영역 가능성
3. 정책·제도적 함의 (~200자):
   - 변호사법, 회계감사법 등 규제 변화 필요성

[Chapter 8 Structure]
1. 핵심 발견 요약 (~300자):
   - 5대 변수가 도입 속도를 설명
   - 가설 검증 결과
2. 본 연구의 의의 (~200자):
   - 비교 프레임워크의 기여

[Constraints]
- Ch.1 한계 명시 필수 (저자 신뢰도 증가)
- Ch.7 "향후 전망"은 단정 금지, "가능성 있다", "추정된다" 표현
- Ch.8 새로운 정보 도입 금지 (요약만)
- 클리셰 금지
- "2026년 5월 기준" 시점 명시

[Output Validation]
- Ch.1: 5개 단락 모두 존재, 한계 명시
- Ch.7: 한국 시장 함의 + 전망 + 정책 함의
- Ch.8: 요약만, 신규 정보 없음

[Output Files]
- /docs/01_intro.md
- /docs/07_implications.md
- /docs/08_conclusion.md
- /reports/day4_task2_report.md
```

---

## Task 4.3: 전체 통합 + Devil's Advocate Review

```
[Role]
비판적 검토자. 칭찬 금지, 약점만 식별.

[Required Reading]
- /docs/ 폴더의 모든 챕터 (01~08)
- AGENTS.md

[Task]
1. /docs/01~08을 순서대로 통합하여 /docs/full_draft_v1.md 생성
2. 통합본을 처음부터 끝까지 읽으며 약점 식별
3. /reviews/devils_advocate_review.md 작성

[Integration]
챕터 순서: 01 → 02 → 03 → 04 → 05 → 06_comparative_full → 07 → 08
각 챕터 사이에 명확한 헤더 구분.

[Review Criteria]
다음 8개 관점에서 약점 식별:
1. 5대 변수가 충분히 변별력 있는가? 중복되거나 약한 변수는?
2. 산업 간 자료 비대칭이 결론을 왜곡시키는가?
3. 결론이 사례로부터 도출되는가, 미리 정해져 있는가?
4. 한국 시장 특수성이 반영되는가?
5. 저자 편향 (CPA 지망자의 자기 직업 방어 논리) 노출?
6. 클리셰 잔존?
7. 인용·각주 누락?
8. 분량 (총 16매) 충족?

[Review Output Format]
## 1. 약점 리스트
### 약점 1: <제목>
- 위치: /docs/XX.md 단락 X
- 인용: "...문제 구간 직접 인용..."
- 문제: <구체적 진단>
- 보강 제안: <구체적 수정안>

(약점 5개 이상 식별 권장)

## 2. 분량 검증
| 챕터 | 명세 분량 | 실제 글자 수 | 부족/초과 |
|---|---|---|---|
| Ch.1 | 1,500 | XXX | XXX |
| ... |
| 합계 | 16,000 | XXX | XXX |

## 3. 클리셰 검출
검출된 클리셰 리스트 + 위치 + 대체 표현 제안.

## 4. 인용·각주 누락 리스트
출처 명시 누락된 사실 진술 위치.

## 5. 최우선 수정 권장 사항 (3개)
Day 5에 반드시 수정해야 할 우선순위 3개.

[Constraints]
- 칭찬 금지
- 보강 제안은 구체적이어야 함 (추상적 "더 분석 필요" 금지)
- 분량 검증은 정확한 글자 수

[Output Files]
- /docs/full_draft_v1.md
- /reviews/devils_advocate_review.md
- /reports/day4_task3_report.md
```

---

# DAY 5 (토 5/16)

## Task 5.1: Devil's Advocate 반영 + Turnitin 패러프레이즈

```
[Role]
표절 방지 전문가 + 한국어 학술 편집자.

[Required Reading]
- /docs/full_draft_v1.md
- /reviews/devils_advocate_review.md
- AGENTS.md §Plagiarism Risk Zones

[Task]
1. Devil's Advocate 검토에서 식별된 약점 반영
2. Turnitin 위험 구간 패러프레이즈
3. /docs/full_draft_v2.md 생성

[Step 1: Devil's Advocate 반영]
/reviews/devils_advocate_review.md의 "최우선 수정 권장 사항 3개" 반영.
그 외 약점은 시간 허용 시 반영.

[Step 2: Risk Zone 식별 및 패러프레이즈]
AGENTS.md §Plagiarism Risk Zones 우선순위 순서:
1. Agentic AI 정의 (Ch.2) — a16z, Anthropic 출처
   → 본인 LangGraph 실전 경험 기반 재서술
2. 빅4 보도자료 표현 (Ch.3) — 모두 패러프레이즈
3. 클리셰 잔존 — 본인 표현으로 대체
4. 학술 자료 15어 이상 직접 인용 — 분량 축소

[Paraphrase Rules]
- 단순 동의어 치환 금지 ("도입한다" → "들여온다" 같은 표면 변경 금지)
- 문장 구조 자체를 바꿈
- 의미·뉘앙스 보존
- 한국어 학술 톤 유지
- 직접 인용은 15어 이하 + 큰따옴표 + 각주 유지

[Output Format]
1. /docs/full_draft_v2.md — 수정된 본문
2. /reviews/paraphrase_log.md — 처리 로그
   ## Risk Zone 처리 내역
   ### Zone 1: <위치>
   - 처리 전: "..."
   - 처리 후: "..."
   - 처리 이유: ...

[Output Validation]
- 클리셰 0개
- 직접 인용 모두 15어 이하
- 한 출처당 직접 인용 최대 1회
- 한국어 학술 톤 유지

[Output Files]
- /docs/full_draft_v2.md
- /reviews/paraphrase_log.md
- /reports/day5_task1_report.md
```

---

## Task 5.2: 인용·각주·참고문헌 정리

```
[Role]
학술 인용 양식 전문가.

[Required Reading]
- /docs/full_draft_v2.md
- /sources/source_matrix_accounting.md
- /sources/source_matrix_legal.md
- /sources/source_matrix_consulting.md

[Task]
1. 본문의 모든 출처를 각주 번호로 재정렬
2. 참고문헌 리스트 작성
3. /docs/references.md 생성

[Format]
Chicago 17th Edition (Notes-Bibliography style) 기본 적용.
학과 양식 미확정 — 본인이 후속 조정 가능하도록 일관된 양식만 유지.

[각주 양식 예시]
- 영문 자료: ¹ John Smith, "Title," *Journal Name* 12, no. 3 (2024): 45-67.
- 한국어 자료: ² 홍길동, "제목," 『학회지명』 12권 3호 (2024): 45-67.
- 웹 자료: ³ EY, "EY.ai Launch," September 13, 2023, https://ey.com/...

[Bibliography 양식]
- 알파벳·가나다순
- 저자 - 제목 - 출판처 - 연도 - URL (있는 경우)

[Task Detail]
1. 본문 처음부터 끝까지 읽으며 모든 각주 번호 1부터 재매김 (중복 출처는 "Ibid." 또는 "ibid.")
2. 참고문헌은 알파벳·가나다순
3. 모든 본문 각주가 참고문헌에 존재하는지 검증
4. 모든 참고문헌이 본문에 인용되는지 검증 (미사용 참고문헌 제거)

[Output Files]
- /docs/full_draft_v2.md (각주 번호 재매김 적용)
- /docs/references.md (참고문헌 리스트)
- /reports/day5_task2_report.md

[Output Validation]
- 모든 각주가 참고문헌에 존재
- 모든 참고문헌이 본문에 인용됨
- 양식 일관성
- 각주 번호 연속성
```

---

## Task 5.3: 최종 통합본 생성

```
[Role]
문서 통합 전문가.

[Required Reading]
- /docs/full_draft_v2.md (각주 정리 완료 상태)
- /docs/references.md

[Task]
1. 본문 + 참고문헌을 하나의 마크다운 파일로 통합
2. 챕터 번호·제목 일관성 확인
3. 최종 분량 확인
4. /docs/final_report.md 생성

[Structure]
# 제목 (본인이 추후 결정 - 임시: "전문 지식서비스 산업의 Agentic AI 도입 양상 비교")

## 1. 서론
...

## 2. Agentic AI 개념
...

(전체 챕터)

## 참고문헌
...

[Output Validation]
- 총 분량 15,000자 이상 (15매 이상)
- 챕터 순서 정확 (1→8)
- 각주 번호 연속성
- 참고문헌 포함
- 한국어 학술 톤 일관

[Output Files]
- /docs/final_report.md
- /reports/day5_task3_report.md (최종 분량 검증 보고서)
```

---

# DAY 5 오후 ~ DAY 6 (본인 직접 작업)

**Codex 위임 종료.** 아래는 본인 수행:

1. `/docs/final_report.md` 읽기 → 한 번 더 통독
2. **마크다운 → 워드(.docx) → 한글(.hwp) 변환**
   - 마크다운을 워드로 (pandoc 또는 복사·붙여넣기)
   - 워드에서 표·각주·페이지번호 정상 확인
   - 한글에서 워드 파일 열기
3. **학과 양식 적용**
   - 첨부 양식 파일의 폰트·줄간격·여백 적용
   - 표지·목차 추가 (분량 계산에서 제외)
   - 참고문헌 양식 학과 양식과 일치 확인
4. **Turnitin 사전 검사**
   - 학교 계정 또는 개인 계정으로 1차 제출
   - 7% 초과 시 → Task 5.1 재실행 (위험 구간 재패러프레이즈)
   - 만족 시 → 최종본 확정
5. **일요일 오전 최종 제출**

---

# Trouble-shooting

## Codex 실패 시 대응
| 증상 | 대응 |
|---|---|
| Task가 너무 길어서 일부만 처리 | task를 더 작게 분할 (예: Task 3.1을 글로벌/한국으로 분리) |
| 자료 매트릭스에 없는 사례 등장 | 해당 사례 즉시 제거 + AGENTS.md 제약 강조 후 재실행 |
| 분량 미달 | 구체적 자료(인용·수치)를 추가하라는 지시로 재실행 (단순 "더 길게" 금지) |
| 클리셰 잔존 | 검출된 클리셰를 명시하고 대체하라는 지시로 재실행 |
| 한국어 톤 어색 | "한국 학술 보고서 톤으로 다듬어 달라"는 명시적 지시 |

## 일정 압박 시 우선순위
**버려도 되는 것 (시간 부족 시)**:
- Day 4 Task 4.3 Devil's Advocate (단, Day 5 패러프레이즈는 절대 생략 금지)
- Ch.7 시사점 분량 축소 (1매 → 0.7매)
- 컨설팅 챕터 깊이 (가장 정형성 낮은 챕터 - 분량 축소 시 영향 최소)

**절대 생략 금지**:
- Day 5 Task 5.1 (Turnitin 패러프레이즈)
- Day 5 Task 5.2 (참고문헌 정리)
- 학과 양식 적용
- Turnitin 사전 검사
