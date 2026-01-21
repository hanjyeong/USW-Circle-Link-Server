# 🌕 동구라미
> **수원대학교 동아리 모집 및 지원 서비스**
> 
> 반복적인 동아리 모집과 지원 절차를 간소화하여 학생들이 더 편리하게 동아리 활동을 이용할 수 있도록 구축된 서비스입니다.

<p align="center">
  <img width="1024" height="500" alt="image" src="https://github.com/user-attachments/assets/5e9f9dcd-717a-4f33-843b-4a1d985e53b4" />
</p>

- **웹사이트**: [동구라미 웹페이지 바로가기](https://donggurami.net/)
- **앱 스토어**: [iOS 앱 스토어 바로가기](https://apps.apple.com/kr/app/%EB%8F%99%EA%B5%AC%EB%9D%BC%EB%AF%B8/id6692607046)

---

## 🗃️ 목차
- 1. [프로젝트 개요](#1-프로젝트-개요)
- 2. [프로젝트 시스템 아키텍쳐](#2-프로젝트-시스템-아키텍쳐)
- 3. [기술 스택](#3-기술-스택)
- 4. [주요 기능 정리](#4-주요-기능-정리)
- 5. [담당 기능 및 적용 기술](#5-담당-기능-및-적용-기술)
- 6. [ERD](#6-erd)
- 7. [트러블 슈팅 및 해결과정](#7-트러블-슈팅-및-해결과정)
- 8. [팀 구성](#8-팀-구성)
- 9. [실제 서비스 화면](#9-실제-서비스-화면)
- 10. [느낀점 및 회고](#10-느낀점-및-회고)

---

## 1. 프로젝트 개요
- **프로젝트 이름** : 동구라미
- **프로젝트 목적** : 반복적인 동아리 모집과 지원 절차를 간소화하여 수원대학교 학생들이 동아리 활동을 더 편리하게 이용할 수 있도록 하였습니다.

### 프로젝트 기획 배경
<img width="717" height="403" alt="배경1" src="https://github.com/user-attachments/assets/3b28aefd-2e00-411a-bdeb-36e3b59abb15" />
<img width="717" height="403" alt="배경2" src="https://github.com/user-attachments/assets/38f50db3-be81-4fce-af2a-a5da7b6b1f92" />
<img width="717" height="403" alt="배경3" src="https://github.com/user-attachments/assets/856db597-d0d4-4804-8f2f-787f83276b89" />

---

## 2. 프로젝트 시스템 아키텍쳐
<img width="802" height="425" alt="System Architecture" src="https://github.com/user-attachments/assets/af95256c-bc91-4ae6-abc4-9480c33ad63c" />

- AWS EC2에서 Spring Boot 애플리케이션 운영
- RDS(MySQL) 관계형 데이터 관리
- Redis 기반 인증 코드 관리 및 분산 환경 대응
- Nginx 리버스 프록시 구성
- FCM을 통한 푸시 알림 서비스

---

## 3. 기술 스택

### Backend
- Java 17
- Spring Boot 3.3.1
- Spring Data JPA / Hibernate
- MySQL 8.0 (AWS RDS)
- Redis 7.0.15
- Firebase Cloud Messaging

### Infra / DevOps
- AWS EC2 (Ubuntu 22.04)
- AWS S3
- Docker
- Nginx

### Collaboration
- Git / GitHub

---

## 4. 주요 기능 정리
- **인증 시스템**: 학교 웹 메일(SMTP)을 통한 학생 전용 회원가입 및 JWT 기반 토큰 관리
- **모집 관리**: 동아리별 모집 상태(모집 중/완료) 조회 
- **지원서 작성**: 지원서 작성 및 지원 가능 
- **검색 및 필터링**: 분야/모집 상태별 동아리 필터링 
- **알림 서비스**: FCM을 활용한 합격/불합격 결과 푸시 알림 전송

---

## 5. 담당 기능 및 적용 기술

   
- **이메일 전송 기반 인증 기능 구현**
    - Spring Mail 활용
    - 인증 코드 생성 및 TTL 관리 (Redis)
    - 회원가입, 아이디/비밀번호 찾기, 회원 탈퇴 인증 처리
- **API 요청 횟수 제한 (Rate Limiting)**
    - Bucket4j 적용, Redis 기반 분산 환경 지원
- **DTO 입력값 검증 구조 설계**
    - ValidationGroup 활용, 상황별 필드 검증 분리
- **Enum 필드값 유효성 검사**
    - 커스텀 Validator/어노테이션 구현, 잘못된 값 사전 차단
- **공통 예외 처리 구조 적용**
    - @ControllerAdvice 기반 전역 예외 처리
    - Custom Exception 및 공통 에러 응답 포맷 적용

---

## 6. ERD
*(여기에 ERD 이미지 주소 또는 마크다운 삽입)*

---

## 7. 트러블 슈팅 및 해결과정
- **이메일 발송 장애**: SMTP 서버 설정 오류 해결
- **API Rate Limiting 도입**: Bucket4j 선정 이유, Redis 연동 문제 해결
- **분산 스케줄링**: Spring Scheduler → Redis 기반 관리 체계로 전환
- **트랜잭션 이슈**: EmailToken 생성 시점과 DB 반영 시점 불일치 문제 해결
- **참조 무결성 오류**: 회원 탈퇴 시 연관 데이터 삭제 정책(Cascade/OrphanRemoval) 수정
- **Bean 생성 오류**: JavaMailSender Config 클래스 충돌 해결
- **Auto Increment 초기화 및 DB 부하 문제 개선**

---

## 8. 팀 구성
| 구분 | 성명 |
|:---:|:---|
| **BE (Web/Mobile)** | 김지오, 남궁다연, 방혁, 한지형 |
| **Design** | 이보영 |
| **FE (Web)** | 이동수, 박성재, 노경미, 김수민 |
| **FE (Mobile)** | 정우창, 유지석, 이수빈 |

---

## 9. 실제 서비스 화면
<p align="center">
  <img width="220" alt="메인페이지" src="https://github.com/user-attachments/assets/fea786a1-5138-40c1-a618-fa3a9877cefc" />
  <img width="220" alt="동아리 지원하기" src="https://github.com/user-attachments/assets/6ec554bb-4bf3-4dd4-8120-453a70543680" />
  <img width="220" alt="푸시 알림" src="https://github.com/user-attachments/assets/b68ff716-8cca-4a37-9761-1c2370e88949" />
</p>
<p align="center">
  <b>[동아리 조회]</b> &nbsp; | &nbsp; <b>[동아리 지원]</b> &nbsp; | &nbsp; <b>[지원 결과 알림]</b>
</p>

---

## 10. 느낀점 및 회고
*(프로젝트 진행 중 배운 점, 성과, 아쉬운 점 등을 자유롭게 작성)*
