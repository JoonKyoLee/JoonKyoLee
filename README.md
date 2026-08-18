## 🙋🏻 About me

**동작하는 코드보다, 오래 운영할 수 있는 구조를 고민하는 백엔드 개발자입니다.**

기능 구현에서 멈추지 않고 "왜 이런 구조가 필요한지"를 먼저 고민합니다.
배포와 운영까지 직접 다루며, 안정적으로 운영되는 서비스를 만드는 데 관심이 많습니다.

## 📌 Projects

- **[뭉치장](https://github.com/MOONGCHIJANG/moongchijang-BE)** | `2026.03 – 2026.06` · 큐시즘
  <details>
  <summary><b>문제 해결 과정 & PR</b></summary>

  <br>

  **🔐 동시성 하에서 결제/환불 정합성 설계와 실험적 검증**
  - 승인, 취소 흐름의 동시성 문제를 정의하고 정합성 처리 기반 구축
    [![PR90](https://img.shields.io/badge/PR-%2390-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/90)
    [![PR96](https://img.shields.io/badge/PR-%2396-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/96)
    [![PR117](https://img.shields.io/badge/PR-%23117-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/117)
  - 상태 전이와 환불 후처리 과정의 정합성 보강
    [![PR143](https://img.shields.io/badge/PR-%23143-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/143)
    [![PR261](https://img.shields.io/badge/PR-%23261-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/261)
  - 실제 시나리오 기반 정합성 실험 및 락 튜닝 수행
    [![PR379](https://img.shields.io/badge/PR-%23379-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/379)

  &nbsp;

  **⚡ Redis Lua 스크립트로 실시간 활성 조회자 집계 원자화**
  - 다중 Redis 왕복을 Lua 단일 호출로 원자화하고, 존재 캐시로 DB 부하 분리
    [![PR93](https://img.shields.io/badge/PR-%2393-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/93)
    [![PR232](https://img.shields.io/badge/PR-%23232-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/232)

  &nbsp;

  **📮 트랜잭션 커밋 이후 알림 후처리 분리 (outbox 성격)**
  - AFTER_COMMIT 분리와 DB 재시도 이력으로 재시작 후에도 이어지는 구조
    [![PR150](https://img.shields.io/badge/PR-%23150-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/150)
    [![PR258](https://img.shields.io/badge/PR-%23258-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/258)
    [![PR299](https://img.shields.io/badge/PR-%23299-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/299)

  &nbsp;

  **🔁 멀티 인스턴스 환경의 상태 전이 중복 실행 제어**
  - 분산락과 배치 REQUIRES_NEW로 중복 실행 방지, 장시간 단일 트랜잭션 회피
    [![PR143](https://img.shields.io/badge/PR-%23143-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/143)

  &nbsp;

  **🚀 Docker 배포 파이프라인 속도와 안정성 개선**
  - Docker 배포 속도 개선 (빌드 책임 분리, 캐시)
    [![PR25](https://img.shields.io/badge/PR-%2325-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/25)
  - 계층형 JAR 기반 이미지 구조 적용
    [![PR30](https://img.shields.io/badge/PR-%2330-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/30)
  - 배포 후 미사용 Docker 이미지 정리 추가
    [![PR32](https://img.shields.io/badge/PR-%2332-181717?logo=github)](https://github.com/MOONGCHIJANG/moongchijang-BE/pull/32)

  </details>
- **[재고관리 시스템](https://github.com/almang2/inventory-server)** | `2025.08 – 2025.12` · 테크포임팩트 × 알맹상점
  <details>
  <summary><b>문제 해결 과정 & PR</b></summary>

  <br>

  **🔐 동시 재고 변경 정합성 제어 (비관적 락)**
  - 동시 재고 변경 구간에 PESSIMISTIC_WRITE 락 적용
    [![PR194](https://img.shields.io/badge/PR-%23194-181717?logo=github)](https://github.com/almang2/inventory-server/pull/194)

  &nbsp;

  **⚡ fetch join으로 목록 조회 N+1 제거**
  - Order, Receipt, Inventory 목록 조회 SQL 감소 (354→5, 228→4, 54→4회)
    [![PR195](https://img.shields.io/badge/PR-%23195-181717?logo=github)](https://github.com/almang2/inventory-server/pull/195)

  &nbsp;

  **📤 대량 소매 업로드 배치 조회와 부분 성공 처리**
  - N+1 제거, 배치 조회/Map 캐시 적용
    [![PR190](https://img.shields.io/badge/PR-%23190-181717?logo=github)](https://github.com/almang2/inventory-server/pull/190)
  - 업로드 트랜잭션 경계 분리, skip 결과 구조화
    [![PR191](https://img.shields.io/badge/PR-%23191-181717?logo=github)](https://github.com/almang2/inventory-server/pull/191)

  </details>
- **[MOOI](https://github.com/Emotion-Storage/mooi-server)** | `2025.06 – 2026.03`

## 🌍 Open Source

- **[apache/airflow](https://github.com/apache/airflow)** | [한국어 번역(i18n) 기여](https://github.com/apache/airflow/pull/70767)

## 🏆 Awards

- **대상** · 큐시즘 33기 밋업데이 | `2026.06` · [MOONGCHIJANG](https://www.moongchijang.com/)
- **최우수상** · 큐시즘 × 씨그로 주식회사 | `2026.03` · [Litmers](https://litmers.com/)
- **장려상** · 재단법인NSI | `2026.08` · [ZEROST](https://github.com/team-0st/BE)

## 👥 Activities

- KUSITMS 33기 | `2026.02 – 2026.06`

## 📜 Certifications

- SQLD | `2026.03`
- 정보처리기사 | `2025.09`
- ADsP | `2025.06`

## 🛠 Tech Stack

![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=openjdk&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)
<br>
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
<br>
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
<br>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=for-the-badge&logo=terraform&logoColor=white)

---

<div align="center">
  <a href="https://git.io/streak-stats">
    <img src="https://streak-stats.demolab.com?user=JoonKyoLee&theme=default&hide_border=true" width="480" />
  </a>
</div>
