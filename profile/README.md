<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
<div align="center">
  <h1>🛒 데이터로 장바구니를 바꾸다</h1>
  <p>🔍 합리적 소비 의사결정 지원을 위한 농수산물 물가 정보 통합 분석 플랫폼 </p>
</div>

<br/>

## 🌱 프로젝트 개요
- 농축수산물 공공데이터를 수집·분석·시각화하여, 
소비자의 합리적인 구매 의사결정 돕는 대시보드 구축 프로젝트
> - **프로젝트 주제:** 농수산물 물가 정보 통합 분석 플랫폼
> - **프로젝트 기간:** 2025.12.09 - 2025.01.08

## 🎯 프로젝트 목표
- **ETL/ELT 파이프라인 설계 및 자동화**
    - 공공 API 기반 농수산물 데이터 수집을 위한 ETL(Extract-Transform-Load) 및 ELT 로직을 구현하고 데이터 수집 및 가공 프로세스를 수행하는 자동화 배치 환경을 구축하고자 함
- **로컬에서 AWS로 이어지는 이식 가능한 데이터 파이프라인 구축**
    - 로컬에서 검증된 로직을 AWS 클라우드로 이관하여, 클라우드 이관 전 로컬 환경에서 데이터 정합성 및 파이프라인 안정성을 사전 점검하고자 함.
- **Streamlit 기반 통합 가격정보 대시보드 구현**
    - 파이프라인을 통해 정제된 데이터를 사용자 중심의 인터페이스로 시각화하여, 물가 변동 확인 및 합리적 구매 의사결정을 돕는 분석 도구를 제공함.
 
---

## 🗂️ Repository 소개
각각의 환경(local / aws) 및 책임 영역에 따라 레포를 구분하였습니다.

| **Repository**        | **Role**          | **Description**                                       | 
|:----------------------:|:-----------------:|:------------------------------------------------------:|
| [Threelacha](https://github.com/dev7-team3/Threelacha)   | 로컬 개발 환경     |  로컬 환경에서 데이터 파이프라인 로직을 검증하는 개발 레포  |
| [Threelacha_airflow_dbt](https://github.com/dev7-team3/Threelacha_airflow_dbt) | AWS 운영 환경      | AWS EC2에서 Airflow 기반 데이터 파이프라인을 운영하는 레포 | 
| [Threelacha_streamlit](https://github.com/dev7-team3/Threelacha_streamlit)   | 대시보드 서비스     | AWS에서 분석 결과를 시각화하는 Streamlit 서비스 레포      | 
| [Threelacha_docs](https://github.com/dev7-team3/Threelacha_docs)        | 프로젝트 문서 관리  | 프로젝트 설계와 운영 기록을 관리하는 문서 레포             | 


## 🗜️ 아키텍처 구조
### 1. 로컬 아키텍처 구조
<img width="1273" height="701" alt="local_pipeline" src="https://github.com/user-attachments/assets/49546ea5-34c7-4534-9b02-79b71d5c3f47" />

### 2. AWS 아키텍처 구조
<img width="854" height="536" alt="cloud_pipeline" src="https://github.com/user-attachments/assets/a5eac6f3-5033-43f9-bcd5-659262be8fe3" />


---

## 🧑‍💻 팀원 소개

| **이름**    | **역할**        | **주요업무**        |
|:-----------:|:---------------:|:---------------:|
| [구다혜](https://github.com/dahye83)      | 프로젝트 총괄          | ETL/ELT/대시보드 구현, 데이터모델링 | 
| [김지연](https://github.com/Jiyeon0027)      | github 관리           | ETL/ELT/대시보드 구현, CI/CD 구현 | 
| [박정은](https://github.com/jjung121)      | 로컬환경 관리           | ETL/ELT 로직, CI/CD 구현, 로컬-클라우드 환경 전환 | 
| [정수진](https://github.com/jipipes)      | AWS인프라 관리           | 클라우드 인프라 구축, streamlit 환경 구성 | 


## ⚙️ 기술 스택
- **데이터 파이프라인 및 인프라**

| **구분** | **기술 스택** | **역할 및 활용** |
| --- | --- | --- |
| **언어** | <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=ffffff"/>| 데이터 수집, ETL/ELT 로직 구현 및 데이터 가공 |
| **컨테이너** | <img src="https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white"/> | 파이프라인 구성 요소의 표준화 및 로컬/클라우드 환경의 일관성 유지 |
| **워크플로우** | <img src="https://img.shields.io/badge/Apache%20Airflow-017CEE?style=for-the-badge&logo=Apache%20Airflow&logoColor=white"/> | 데이터 수집 및 배치 파이프라인의 오케스트레이션 및 스케줄링 관리 |
| **데이터 모델링** | <img src="https://img.shields.io/badge/dbt-de5833?style=for-the-badge&logoColor=white"/> | 분석용 데이터 마트 구성을 위한 SQL 기반 데이터 모델링 |
| **쿼리 엔진** | <img src="https://img.shields.io/badge/trino-DD00A1?style=for-the-badge&logo=trino&logoColor=white"/> <img src="https://img.shields.io/badge/aws%20athena-FF7139?style=for-the-badge&logoColor=white"/> | dbt 구동 및 대시보드 연동을 위한 분산 분석 쿼리 엔진 |
| **메타데이터** | <img src="https://img.shields.io/badge/HIVE%20metastore-39477F?style=for-the-badge&logoColor=yellow"/> <img src="https://img.shields.io/badge/AWS%20glue%20catalog-6d4aff?style=for-the-badge&logoColor=white"/> | 데이터 테이블 스키마 및 파티션 정보 관리 (서버리스 메타스토어 활용) |
| **스토리지** | <img src="https://img.shields.io/badge/minio-C72E49?style=for-the-badge&logo=minio&logoColor=white"/> <img src="https://img.shields.io/badge/Amazon%20S3-FF9900?style=for-the-badge&logo=amazons3&logoColor=white"/> | Raw / Silver / Gold 데이터의 단계별 저장소 (로컬: MinIO, AWS: S3) |
| **메타/프로덕션 DB** | <img src="https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/aws%20rds-39477F?style=for-the-badge&logoColor=white"/> | Airflow 메타데이터 저장 및 Gold Layer 데이터 서빙 DB |
| **CI/CD** | <img src="https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white"/> | 코드 변경 시 자동화된 테스트 및 AWS 환경으로의 지속적 배포(CD) 수행 |
| **모니터링** | <img src="https://img.shields.io/badge/aws%20cloudwatch-006f5c?style=for-the-badge&logoColor=white"/> | 인프라 자원 사용량 모니터링 및 메일 통한 알림 시스템 구축 |
| **자동화 운영** | <img src="https://img.shields.io/badge/aws%20lambda-FF6600?style=for-the-badge&logoColor=white"/> | 인프라 비용 절감을 위한 스케줄링 기반 인스턴 (EC2/RDS) 자동 기동/정지 관리 |

- **분석 및 시각화**

| **구분** | **기술 스택** | **역할 및 활용** |
| --- | --- | --- |
| **분석/검증** | <img src="https://img.shields.io/badge/jupyter-%23F37626.svg?style=for-the-badge&logo=jupyter&logoColor=white"/> <img src="https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=black"/> | 데이터 탐색(EDA) 및 ETL 로직 사전 검증 |
| **시각화** | <img src="https://img.shields.io/badge/Streamlit-%23FF4B4B.svg?style=for-the-badge&logo=streamlit&logoColor=white"/> | 통합 정보 대시보드 서비스 구현 |

---

## 📂 문서 자료
- [프로젝트 보고서](https://github.com/dev7-team3/Threelacha_docs/blob/main/%EB%B3%B4%EA%B3%A0%EC%84%9C/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8_%EC%B5%9C%EC%A2%85%EB%B3%B4%EA%B3%A0%EC%84%9C.md)
- [결과 대시보드](https://github.com/dev7-team3/Threelacha_streamlit/blob/main/README.md)
- [트러블 슈팅](https://github.com/dev7-team3/Threelacha_docs/tree/main/troubleshooting)
- [ADR: Architectural Decision Records](https://github.com/dev7-team3/Threelacha_docs/tree/main/ADR)

---
