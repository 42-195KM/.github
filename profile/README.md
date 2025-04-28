<aside>

# 💡서비스/프로젝트 소개
![image (1)](https://github.com/user-attachments/assets/dfc1065b-a1e2-4414-ba80-83f9dc27fdef)

</aside>

> All in One 통합 러닝 서비스입니다.
러닝 기록 관리, 크루 활동, 대회 신청 등 러닝과 관련된 서비스들을 안정적으로 제공합니다.
> 

<aside>

# 🎯서비스/프로젝트 목표

</aside>

**대규모 트레픽 대응**

- MSA 구조로 장애 대응 및 확장성 확보
- Kafka를 이용해 고성능과 고가용성 구현
- Redis로 처리 속도 향상

**안정적인 모니터링**

- Prometheus, Grafna 이용
- 시스템, 어플리케이션 지표 관리

**배포**

- Docker를 이용해 실행 환경 통일, 배포 단순화

<aside>


# 🛠 인프라 설계도

</aside>

`최종(최신화된) 인프라 설계도를 넣어주세요.(MSA 시스템 흐름, CI/CD포함)`

<aside>


# 🔍 주요 기능

</aside>

- **사용자**
    - 사용자 회원가입 및 로그인 처리와 서비스 인증 인가처리 관리
- **러닝 기록**
    - 러닝 기록 등록 및 저장
- **랭킹**
    - 러닝 기록 기반 랭크 시스템, 기록 경쟁 확인
- **업적**
    - 러닝 기록 기반 랭크 시스템, 러닝 목표 달성 유도
- **이용자 보고서 (ReCap)**
    - 러닝 기록 기반 요약 보고서
- **러닝 크루**
    - 러너 간 커뮤니케이션, 모임 모집, 정보 게시판 공유
- **대회**
    - 공식 대회 참여 알림 및 유도
- **챗봇**
    - 사용자가 원하는 러닝 관련 정보 제공
- **알림**
    - 사용자 슬랙 아이디로 대회/업적 이벤트 알림

<aside>


# 🪄 적용 기술

</aside>

`기술과 함께, 해당 기술을 선택한 근거/목적을 함께 작성해주세요.`

| 카테고리 | 기술 | 버전 | 근거/ 목적 |
| --- | --- | --- | --- |
| 언어 | Java | 17 | LTS 지원 최신 언어 |
| 빌드 | Gradle | 1.1.7 | 빌드 관리 자동화 |
| 프레임워크 | Spring Boot | 3.4.4 | 설정 간소화 |
| 라이브러리 | Netflix Eureka | Spring Cloud 2024.0.1 | MSA 환경에서 서비스 인스턴스 자동 등록·검색 |
|  | Spring Boot JPA |  | SQL 없이도 간단히 구현 |
|  | Spring Boot Kafka |  | 비동기 처리하여 서비스 간 결합도를 낮추고 확장성 확보 |
|  | Jackson2JsonRedisSerializer |  | JSON 형태로 저장·조회 |
|  | Swagger(springdoc-openapi) | 2.8.5 | API 명세 자동 생성, 테스트 편의성 |
| Infra | Docker  |  | 개발·테스트 환경 일치 |
|  | PostgreSQL | ankane/pgvector:latest | 벡터 검색 기능 포함 |
|  | Redis | redis/redis-stack |  |
|  | Zookeeper | wurstmeister/zookeeper | 오프셋 관리·파티션 메타데이터 조율 |
|  | Apache Kafka | wurstmeister/kafka | 멱등·재시도 설정 |
| UI | kafka-ui | provectuslabs/kafka-ui |  |
| 모니터링 | Prometheus | prom/prometheus | 메트릭을 스크래핑해 시계열 데이터 수집 |
|  | Grafana | grafana/grafana | 메트릭을 대시보드화 |
|  | Loki | grafana/loki | 로그를 라벨링해 중앙집중식 저장 |
|  | Micrometer Registry Prometheus |  | 모니터링 파이프라인에 연결 |
| Test | Spring Boot Starter Test | JUnit Platform Launcher | 통합 테스트와 연동 테스트 지원 |

<aside>


# 👥 기술적 의사결정

</aside>

- Kafka 도입

- Redis 도입

<aside>


# 🔬 트러블슈팅

</aside>

`부하테스트를 주제로 한 트러블슈팅을 포함해주시고, 내용에는 [before&after 캡쳐본 / 개선된 수치 / 개선방법 / 의사결정 과정]을 포함해주세요.`

<aside>


# ♻️ CONTRIBUTORS
| 팀원명 | 포지션 | 담당 | 깃허브 링크 |
| --- | --- | --- | --- |
| 강민 | 팀원 | ▶ `업적`<br>- | <a href="https://github.com/singingsandhill"><img height="130px" width="130px" src="https://avatars.githubusercontent.com/u/14273642?v=4"/></a> |
| 김도훈 | 팀원 | ▶ `챗봇` <br>- | <a href="https://github.com/singingsandhill"><img height="130px" width="130px" src="https://avatars.githubusercontent.com/u/68257796?v=4"/></a>|
| 김재현 | 팀장 | ▶ `사용자` <br>- JWT를 이용한 인증 / 인가 처리 | <a href="https://github.com/singingsandhill"><img height="130px" width="130px" src="https://avatars.githubusercontent.com/u/94097685?v=4"/></a>|
| 김지수 | 팀원 | ▶ `대회`<br>- Kafka, Redis 기반의 대용량 트레픽 <br>▶ `모니터링`<br>-  |<a href="https://github.com/singingsandhill"><img height="130px" width="130px" src="https://avatars.githubusercontent.com/u/64348312?v=4"/></a>|
| 최해인 | 테크리더 | ▶ `이용자 보고서`<br>- <br>▶ `배포`<br>-  |  <a href="https://github.com/singingsandhill"><img height="130px" width="130px" src="https://avatars.githubusercontent.com/u/113276452?v=4"/></a> |
</aside>
