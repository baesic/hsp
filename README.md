# hsp
HSP & High-Functioning ADHD Self-Test Suite

---

## 🌟 주요 기능 (Key Features)

본 프로젝트는 **HSP(Highly Sensitive Person, 매우 민감한 사람)** 및 **고기능 ADHD(High-Functioning ADHD)** 자가 진단 테스트를 다양한 언어와 공유 기능을 통해 웹에서 편리하게 수행할 수 있도록 구축한 시스템입니다.

---

### A. HSP 테스트 (HSP Tests)

#### 1. 단일 언어 기본 버전 (Single Language Standard Versions)
가장 가볍고 빠르며 단일 언어로 동작하는 기본 테스트 페이지입니다.  
- `New-Self-Test_kor.html` (한국어)
- `New-Self-Test_eng.html` (영어)
- `New-Self-Test_fra.html` (프랑스어)
- `New-Self-Test_chn.html` (중국어)

#### 2. 한국어 공유 특화 버전 (Korean Share-Enabled Version)
- `New-Self-Test_kor2share.html` :
  한국어 베이스 테스트입니다. 테스트 완료 후:
  - **결과 화면 이미지 저장** : `html2canvas`로 결과 영역만 캡처 (공유 버튼 자동 제외)
  - **Web Share API 결과 공유** : 이미지 파일 + 텍스트/링크 동시 공유, 미지원 브라우저에서는 클립보드 복사 폴백
  - **이미지 로컬 다운로드** : 고화질 PNG로 결과 이미지 저장

#### 3. [추천] 멀티 다국어 & 통합 공유 완전판 (Multilingual & Global Sharing Version)
**가장 최적화되고 모든 오류가 디버깅된 검증된 완전판 버전입니다.**  
- `New-Self-Test_ml2share.html` : 
  - **실시간 다국어 지원**: 한국어(ko), 영어(en), 프랑스어(fr), 중국어(zh), 일본어(ja)를 테스트 중이나 결과창 도중 언제든 실시간 전환할 수 있습니다. 
  - **결과 하위 척도(Subscale) 분석 계산**: 18문항의 응답값을 기반으로 6개 세부 카테고리(과도한 자극, 긍정적 경험 민감성, 사회적 민감성, 정보 처리 깊이, 정서적 반응성, 세부 사항 민감성) 점수를 완벽히 추산하여 분석을 제공합니다.
  - **URL 파라미터 기반 특정 언어 공유**: 공유 시 현재의 언어(`?lang=자국어`)가 URL로 자동 할당
  - **결과 이미지 캡처 및 다운로드**: 결과 화면만 캡처 (공유 버튼 자동 제외), 고화질 PNG로 저장
  - **다중 공유 지원**: Web Share API (이미지+텍스트+링크), 미지원 브라우저에서는 `navigator.clipboard` 자동 복사 + `prompt()` 수동 복사 폴백
  - **localStorage 언어 저장**: 선택한 언어가 브라우저에 저장되어 다음 방문 시에도 유지

---

### B. 고기능 ADHD 테스트 (High-Functioning ADHD Test) ✨ NEW

#### 4. ADHD 다국어 공유 완전판 (ADHD Multilingual & Sharing Version)
- `New-Self-Test_adhd_ml2share.html` :
  ASRS-v1.1 (Adult ADHD Self-Report Scale) 18문항 기반의 고기능 ADHD 선별 테스트입니다.
  - **ASRS-v1.1 전체 18문항**: Part A (6문항 선별 검사) + Part B (12문항 임상 참고)
  - **실시간 다국어 지원**: 한국어(ko), 영어(en), 프랑스어(fr), 중국어(zh), 일본어(ja) 5개 언어 실시간 전환
  - **Part A 선별 채점**: 문항별 차등 임계값 적용 (Q1-3: ≥2, Q4-6: ≥3), 4개 이상 = "ADHD와 높은 일치"
  - **하위 척도 분석**: 주의력 결핍(Inattention, 9문항) / 과잉행동-충동성(Hyperactivity-Impulsivity, 9문항)
  - **고기능 ADHD 맥락**: 보상 전략으로 인해 선별 점수가 낮을 수 있음을 안내
  - **결과 이미지 캡처/공유/다운로드**, **URL 파라미터 언어 공유**, **localStorage 언어 저장** 지원
  - **보라색(Purple) 테마**로 HSP 테스트와 시각적 구분

---

### C. HSP + ADHD 융합 테스트 (Combined HSP & ADHD Test) ✨ NEW

#### 5. [추천] 융합 다국어 공유 완전판 (Combined Multilingual & Sharing Version)
- `New-Self-Test_combined_ml2share.html` :
  HSP-R (18문항) + ASRS-v1.1 (18문항) = **총 36문항**을 한 번에 수행하여 HSP와 고기능 ADHD를 동시에 분석합니다.
  - **통합 분석 결과**: HSP+ADHD 모두 높은 경우 "민감한 ADHD" 유형 해석, 한쪽만 높은 경우 맞춤 해석, 모두 낮은 경우에도 고기능 ADHD 보상 전략 안내
  - **HSP 결과**: 총점/평균 + 6개 하위 척도 (과도한 자극, 긍정적 경험 민감성, 사회적 민감성, 정보 처리 깊이, 정서적 반응성, 세부 사항 민감성)
  - **ADHD 결과**: Part A 선별(양성/음성) + 총점/평균 + 2개 하위 척도 (주의력 결핍, 과잉행동-충동성)
  - **실시간 5개 언어 전환**, **결과 이미지 캡처/공유/다운로드**, **URL 파라미터 공유**, **localStorage 언어 저장**
  - **인디고(Indigo) 테마**로 HSP(파란색)와 ADHD(보라색) 결합 디자인

---

## 📋 저작권 및 출처 (Copyright & Attribution)

### HSP-R (Highly Sensitive Person Scale - Revised)

이 온라인 테스트는 Pluess, M., Aron, E., 외 (2024)의 'Highly Sensitive Person Scale - Revised (HSP-R)' PDF 설문지를 기반으로 하여, 사용자들이 온라인에서 편리하게 자가 평가를 진행할 수 있도록 각색한 것입니다. 원본 연구 및 설문지의 저작권을 존중하며, 이 웹 버전은 개인의 이해와 교육적 목적으로만 사용해주시기 바랍니다.

The original Highly Sensitive Person self-test by Dr. Elaine Aron, which this revised scale builds upon, can also be found at: [https://hsperson.com/test/highly-sensitive-test/](https://hsperson.com/test/highly-sensitive-test/)

**Reference for the HSP-R Scale:**

Pluess, M., Aron, E., Kähkönen, J. E., Lionetti, F., Huang, Y., Tillmann, T., Greven, C., & Aron, A. (2024). Evolution of the Concept of Sensitivity and its Measurement: The Highly Sensitive Person Scale-Revised. PsyArXiv. [https://osf.io/preprints/psyarxiv/w7bqu](https://osf.io/preprints/psyarxiv/w7bqu).
(Note: This is a preprint version and has not yet undergone peer review. Please check online after mid-2025 for the citation of the published article.)

This questionnaire (HSP-R) is protected by copyright laws. Unauthorized modifications are strictly prohibited. Permission is granted to reproduce this questionnaire for personal, clinical, educational, and research purposes, provided the conditions from the original authors are met (including citing the full reference and linking to their websites).

For more information on sensitivity research and the HSP trait, please visit:
* [https://sensitivityresearch.com/](https://sensitivityresearch.com/)
* [https://hsperson.com/](https://hsperson.com/)

### ASRS-v1.1 (Adult ADHD Self-Report Scale)

**© New York University and Ronald C. Kessler, PhD. All rights reserved.**

ASRS-v1.1은 세계보건기구(WHO)와의 협력 하에 다음 연구자들에 의해 개발되었습니다:
- **Lenard Adler, MD** — New York University Medical School
- **Ronald C. Kessler, PhD** — Harvard Medical School
- **Thomas Spencer, MD** — Harvard Medical School

**공익성 안내 (Public Interest Notice):**

본 프로젝트에 포함된 ADHD 테스트는 WHO 공동 개발 ASRS-v1.1 척도를 기반으로, **개인의 자기 이해와 교육적 목적**으로 제공됩니다. 이 도구는 의학적 진단을 대체하지 않으며, 정확한 진단은 반드시 전문가와 상담해야 합니다.

'고기능 ADHD(High-Functioning ADHD)'란 보상 전략(compensatory strategies)으로 인해 일상 기능을 유지하면서도 ADHD 증상을 보이는 경우를 말합니다. 이러한 개인들은 선별 도구에서 낮은 점수를 받더라도 내면의 에너지 소모와 어려움을 경험할 수 있습니다.

The ADHD tests in this project are based on the WHO co-developed ASRS-v1.1 scale, provided for personal self-understanding and educational purposes only. This tool does not replace professional medical diagnosis. 'High-Functioning ADHD' refers to individuals who maintain daily functioning through compensatory strategies while exhibiting ADHD symptoms.

ASRS-v1.1 허가 문의: [ronkadm@hcp.med.harvard.edu](mailto:ronkadm@hcp.med.harvard.edu)

For more information:
* [WHO — World Health Organization](https://www.who.int/)
* [ADDA — Attention Deficit Disorder Association](https://add.org/)

---
