---
name: epic-writer
description: Use when writing an epic document (대규모 장기 프로젝트 기획서) with Problem/Background/End Picture/Impact/Roadmap structure
---

# Epic Writing Skill

An epic document is a planning artifact for large, multi-phase projects. Unlike a PRD (single feature or fix), an epic spans multiple PRDs, takes months to years, and requires a decision-maker to commit to a long-term direction.

The five-section structure:

  # Problem
  # Background
  # End Picture
  # Impact
  # Roadmap

---

## 핵심 원칙 (모든 섹션에 적용)

**prd-writer 스킬의 모든 문체·용어 원칙이 그대로 적용됩니다.**
- ~합니다 / ~습니다 체(경어체) 일관 사용
- 확신도에 따른 어미 구분: 사실 → ~합니다, 가능성 → ~수 있습니다
- 영어 용어는 영어 그대로, 괄호 병기는 최초 1회만
- 구체성: 막연한 문장 → 구체적 동작·이름·숫자로 교체
- 모르면 솔직하게: `** 확인 필요`로 인라인 표기

**DARO 공유 컨텍스트는 prd-writer 스킬을 참조합니다.** Background에서 재설명하지 않습니다.

---

## PRD vs Epic 차이

| | PRD | Epic |
|---|---|---|
| 범위 | 단일 기능·수정 | 다단계 장기 프로젝트 |
| 주요 독자 | 담당 엔지니어 | 의사결정권자 + 개발팀 |
| 기간 | 1~4주 | 수개월 ~ 수년 |
| 결과물 | 구현 명세 | 방향성 + 단계 계획 + PRD 목록 |
| Solution 섹션 | 구현 상세 포함 | 없음 (Roadmap + PRD 링크로 대체) |
| End Picture | 없음 | **필수** — 완전 완료 시의 비전 |

---

## Stage 1: Context Gathering

prd-writer의 맥락 수집에 추가로 파악합니다:

1. **End Picture 시점은 언제인가?** (몇 년 후를 보고 있는가)
2. **주요 의사결정권자는 누구인가?** (이 문서로 누구를 설득해야 하는가)
3. **현재 어느 단계인가?** (MVP 전, MVP 중, 첫 Phase 완료 후 등)
4. **각 Phase의 성공 기준이 있는가?**
5. **이미 작성된 연결 PRD가 있는가?**

---

## Stage 2: 섹션별 작성 가이드

### Problem

**prd-writer의 Purpose와 동일한 기준.** 1문장, 절 2개 이하.

Epic이므로 개별 기능 결함보다 **구조적·전략적 문제**를 다룹니다.

좋은 예:
> "DARO는 SSP로만 기능해 수요 측 수익의 상당 부분이 외부 DSP로 유출되며, 퍼블리셔와의 장기 관계를 강화할 lock-in 수단이 없습니다."

---

### Background

**prd-writer의 Background 규칙과 동일.** 5줄 이내, 상세는 토글.

Epic에서 추가로 포함할 것:
- 이 문제가 발생하는 **전략적·사업적 맥락** (시장 구조, 경쟁 환경)
- 이미 완료된 관련 작업이 있다면 1줄 언급

피할 것:
- 해결 방향 제시 ("~구조가 필요합니다", "~를 도입해야 합니다")
- DARO 공유 컨텍스트 재설명

---

### End Picture

**Epic의 핵심 섹션.** 이 섹션의 퀄리티가 의사결정권자의 장기 투자 결정을 좌우합니다.

> **End Picture ≠ Impact**
> Impact는 "문제가 해결된 상태"입니다.
> End Picture는 "이 Epic이 완전히 완료됐을 때 세상이 어떻게 보이는가" — 완성된 비전입니다.

**기준**: 의사결정권자가 이 그림을 읽고 "이걸 달성하기 위해 몇 년이 걸려도 기다릴 수 있다"는 확신이 드는 수준.

**End Picture가 반드시 답해야 하는 4가지 질문:**

1. **누가 무엇을 하고 있는가?** 구체적 사용자·파트너·고객의 행동
2. **어떤 지표가 달성되어 있는가?** 수익·시장 점유·고객 수 등 정량 목표
3. **어떤 시장 포지션을 갖고 있는가?** 경쟁 구도에서 DARO의 위치
4. **어떤 운영 구조가 작동하고 있는가?** 조직·시스템·파트너십의 상태

**포맷 (서술 + 구조화 혼합):**
```
### End Picture

[2-3문장 서술: 최종 시점의 전체 그림 — 숫자와 구체적 주어 포함]

#### 고객 / 파트너
- [구체적 행동 묘사 — "~하고 있습니다" 형태]

#### 핵심 지표 (목표)
| 지표 | 현재 | End Picture |
|---|---|---|
| ... | ... | ... |

#### 시장 포지션
- [경쟁 구도에서의 위치]

#### 운영 구조
- [어떤 시스템·팀·파트너십이 작동하는지]
```

**End Picture에서 피할 것:**
- Phase별 진행 계획 → Roadmap으로
- 기술 구현 상세 → 각 Phase PRD로
- "기여합니다", "향상됩니다" 같은 추상 동사로만 끝내는 것
- Impact와 내용이 겹치는 것 ("문제가 해결된 상태" ≠ "완성된 비전")

---

### Impact

**"이 Epic이 완료되면 어떤 비즈니스 변화가 생기는가."**

prd-writer의 Impact와 동일한 기준이지만, **전략적 수준의 변화**를 다룹니다.

- 숫자가 있으면 AS-IS / TO-BE 테이블
- 숫자가 없으면 bullet 3개 이하, 각 1문장
- "기능적 변화" / "비즈니스 변화" 소헤더 없음
- Solution 기능이나 End Picture 비전을 언급하지 않음 — Impact는 오직 "문제가 없어진 상태"

---

### Roadmap

**Epic을 구성하는 Phase 목록.** 각 Phase는 독립적으로 가치를 제공해야 합니다.

**포맷:**
```
### Phase 1: [이름] — [예상 기간 또는 분기]
[1문장: 이 Phase가 달성하는 것]
PRD: [링크 또는 "미작성"]

### Phase 2: [이름] — [예상 기간]
[1문장]
PRD: [링크 또는 "미작성"]

### Out of Scope (이번 Epic에서 제외)
- [명시적으로 제외하는 항목들]
```

**Roadmap 원칙:**
- Phase 내 구현 상세 없음 → PRD가 담당
- 각 Phase는 독립적으로 배포·롤백 가능한 단위
- Phase 2 이후는 유동적임을 명시해도 됨

---

## Stage 3: Self-Check

**Problem**
- [ ] 1문장, 절 2개 이하인가?
- [ ] Epic 수준의 구조적·전략적 문제인가?
- [ ] ~합니다 체로 끝맺는가?

**Background**
- [ ] 5줄 이내인가?
- [ ] 해결 방향 제시 없는가? ("~가 필요합니다" 금지)
- [ ] DARO 공유 컨텍스트를 재설명하지 않는가?

**End Picture**
- [ ] 4가지 질문(누가 무엇을·지표·포지션·운영구조)에 모두 답하는가?
- [ ] Phase 계획이나 기술 구현이 섞여 있지 않는가?
- [ ] Impact와 내용이 겹치지 않는가?
- [ ] 의사결정권자가 이 그림을 보고 장기 투자를 결정할 수 있는 수준인가?
- [ ] 추상 동사("기여", "향상", "개선")로만 끝나는 문장이 없는가?

**Impact**
- [ ] End Picture나 Solution 기능이 아닌, 문제가 해결된 상태인가?
- [ ] 전략적 수준의 변화를 다루는가?
- [ ] Bullet 3개 이하 또는 AS-IS/TO-BE 테이블인가?

**Roadmap**
- [ ] 각 Phase가 독립적으로 가치를 제공하는가?
- [ ] Phase 내 구현 상세가 없는가?
- [ ] Out of Scope가 명시되어 있는가?

**문체 (전체)**
- [ ] ~합니다 / ~습니다 체로 일관되는가?
- [ ] 확실한 사실 → ~합니다, 가능성 → ~수 있습니다로 구분되는가?

---

## Stage 4: Notion 작성

prd-writer의 Stage 4와 동일한 절차를 따릅니다.

---

**관련 스킬**:
- 단일 기능·수정 문서는 `prd-writer` 스킬을 사용합니다.
- GTM 전략·시장 진입·포지셔닝 등 전략 문서는 `strategy-writer` 스킬을 사용합니다.
