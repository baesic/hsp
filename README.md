# hsp
HSP New Self-test

---

## 🌟 주요 기능 (Key Features)

본 프로젝트는 **HSP(Highly Sensitive Person, 매우 민감한 사람) 자가 진단 테스트**를 다양한 언어와 공유 기능을 통해 웹에서 편리하게 수행할 수 있도록 구축한 시스템입니다.  

### 1. 단일 언어 기본 버전 (Single Language Standard Versions)
가장 가볍고 빠르며 단일 언어로 동작하는 기본 테스트 페이지입니다.  
- `New-Self-Test_kor.html` (한국어)
- `New-Self-Test_eng.html` (영어)
- `New-Self-Test_fra.html` (프랑스어)
- `New-Self-Test_chn.html` (중국어)

### 2. 한국어 공유 특화 버전 (Korean Share-Enabled Version)
- `New-Self-Test_kor2share.html` :
  한국어 베이스 테스트입니다. 테스트 완료 후:
  - **결과 화면 이미지 저장** : `html2canvas`로 결과 영역만 캡처 (공유 버튼 자동 제외)
  - **Web Share API 결과 공유** : 이미지 파일 + 텍스트/링크 동시 공유, 미지원 브라우저에서는 클립보드 복사 폴백
  - **이미지 로컬 다운로드** : 고화질 PNG로 결과 이미지 저장

### 3. [추천] 멀티 다국어 & 통합 공유 완전판 (Multilingual & Global Sharing Version)
**가장 최적화되고 모든 오류가 디버깅된 검증된 완전판 버전입니다.**  
- `New-Self-Test_ml2share.html` : 
  - **실시간 다국어 지원**: 한국어(ko), 영어(en), 프랑스어(fr), 중국어(zh), 일본어(ja)를 테스트 중이나 결과창 도중 언제든 실시간 전환할 수 있습니다. 
  - **결과 하위 척도(Subscale) 분석 계산**: 18문항의 응답값을 기반으로 6개 세부 카테고리(과도한 자극, 긍정적 경험 민감성, 사회적 민감성, 정보 처리 깊이, 정서적 반응성, 세부 사항 민감성) 점수를 완벽히 추산하여 분석을 제공합니다.
  - **URL 파라미터 기반 특정 언어 공유**: 공유 시 현재의 언어(`?lang=자국어`)가 URL로 자동 할당되어, 링크를 누른 제3자도 내가 공유한 언어로 즉시 페이지가 열리도록 언어 선택-공유 연동 기능이 완벽하게 보정(디버깅)되었습니다.
  - **결과 이미지 캡처 및 다운로드**: 결과 화면만 캡처 (공유 버튼 자동 제외), 고화질 PNG로 저장
  - **다중 공유 지원**: Web Share API (이미지+텍스트+링크), 미지원 브라우저에서는 `navigator.clipboard` 자동 복사 + `prompt()` 수동 복사 폴백
  - **localStorage 언어 저장**: 선택한 언어가 브라우저에 저장되어 다음 방문 시에도 유지

---

**안내 및 출처 정보**

이 온라인 테스트는 Pluess, M., Aron, E., 외 (2024)의 'Highly Sensitive Person Scale - Revised (HSP-R)' PDF 설문지를 기반으로 하여, 사용자들이 온라인에서 편리하게 자가 평가를 진행할 수 있도록 각색한 것입니다. 원본 연구 및 설문지의 저작권을 존중하며, 이 웹 버전은 개인의 이해와 교육적 목적으로만 사용해주시기 바랍니다.

The original Highly Sensitive Person self-test by Dr. Elaine Aron, which this revised scale builds upon, can also be found at: [https://hsperson.com/test/highly-sensitive-test/](https://hsperson.com/test/highly-sensitive-test/)

**Reference for the HSP-R Scale used in this adaptation:**

Pluess, M., Aron, E., Kähkönen, J. E., Lionetti, F., Huang, Y., Tillmann, T., Greven, C., & Aron, A. (2024). Evolution of the Concept of Sensitivity and its Measurement: The Highly Sensitive Person Scale-Revised. PsyArXiv. [https://osf.io/preprints/psyarxiv/w7bqu](https://osf.io/preprints/psyarxiv/w7bqu).
(Note: This is a preprint version and has not yet undergone peer review. Please check online after mid-2025 for the citation of the published article.)

This questionnaire (HSP-R) is protected by copyright laws. Unauthorized modifications are strictly prohibited. Permission is granted to reproduce this questionnaire for personal, clinical, educational, and research purposes, provided the conditions from the original authors are met (including citing the full reference and linking to their websites).

For more information on sensitivity research and the HSP trait, please visit:
* [https://sensitivityresearch.com/](https://sensitivityresearch.com/)
* [https://hsperson.com/](https://hsperson.com/)

---
