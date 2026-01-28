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
- 6. [트러블 슈팅 및 해결과정](#7-트러블-슈팅-및-해결과정)
- 7. [팀 구성](#8-팀-구성)

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

- **회원가입/로그인**
    - 학교 웹 메일을 이용한 이메일 인증 과정
    - 아이디 중복 검사
    - 프로필 중복 검사 
    - 기존 동아리원 회원가입 / 신규 동아리원 회원가입
    - 로그인/로그아웃
    - 약관 동의 

- **아이디/비밀번호 찾기**
    - 4자리 인증 코드를 이용한 아이디/ 비밀번호 찾기 


- **메인 서비스**
    - 카테고리 설정을 이용한 동아리 필터 기능
    - 모집중 / 모집완료 동아리 조회
    - 동아리별 소개 페이지 조회 
    - 구글 폼 링크를 이용한 동아리 지원
    

- **마이 페이지**
    - 내 정보 수정(프로필 수정, 비밀번호 변경) 
    - 소속된 동아리/지원한 동아리 조회
    - 회원 탈퇴
  
- **동아리 회장 서비스**
    - 동아리 정보 수정
    - 동아리 소개글 작성(사진 등록, 모집중/모집 완료 상태 설정)
    - 동아리 회원 추가 및 기존 동아리원 가입 요청 관리
    - 지원자 합격/불합격 처리 

- **동아리 연합회 서비스**
  - 동아리방 위치 정보 설정
  - 동아리 카테고리 설정
  - 동아리 회원추가 엑셀 파일 업로드
  - 동아리 추가 및 삭제
  - 공지사항 작성 및 수정
 
- **알림 서비스**
    - 합격/ 불합격 알림 서비스 

<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/82979aca-d646-4d0d-86d5-3c16da8af2de" width="200"></td>
    <td><img src="https://github.com/user-attachments/assets/1636e8e6-6adc-4abf-8275-8cf248f708f3" width="200"></td>
    <td><img src="https://github.com/user-attachments/assets/cd040548-ffed-4e82-a9a3-787af8dad334" width="200"></td>
    <td><img src="https://github.com/user-attachments/assets/eb3405b6-b30f-47f3-b738-aa36bd25bca4" width="200"></td>
    <td><img width="220" alt="동아리 지원하기" src="https://github.com/user-attachments/assets/6ec554bb-4bf3-4dd4-8120-453a70543680" /></td>
    <td><img src="https://github.com/user-attachments/assets/18ea63a6-118f-4755-af1f-246ff73906b8" width="200"></td>
    <td><img width="220" alt="푸시 알림" src="https://github.com/user-attachments/assets/b68ff716-8cca-4a37-9761-1c2370e88949" /></td>
  </tr>
</table>

---

## 5. 담당 기능 및 적용 기술

- **회원가입**
    - Naver Stmp 서버를 이용한 학교 웹 메일 인증
    - Spring JavaMailSender를 이용한 이메일 생성
    - 기존 동아리원 회원과 신규 동아리원 회원 가입 과정 분리 
    - Redis TTL 기능을 이용한 회원가입 토큰 관리 
- **아이디/비밀번호 찾기**
    - 인증 코드 생성
    - Redis TTL 기능을 이용한 인증 토큰 관리 
- **회원 탈퇴**
    - 인증 코드 생성
    - Redis TTL 기능을 이용한 탈퇴 토큰 관리 
  
- **API 요청 횟수 제한**
    - BruteForce 공격을 방어하기 위한 Bucket4j 라이브러리 적용
- **DTO 입력값 검증 구조 설계**
    - SqlInjection 방지를 위한 ValidationGroup 활용, 상황별 필드 검증 분리
- **Enum 필드 값 유효성 검사**
    - 커스텀 Validator/어노테이션 구현, 잘못된 값 사전 차단
- **에러 핸들링**
    - @ControllerAdvice 기반 전역 예외 처리
    - Custom Exception 및 공통 에러 응답 포맷 적용

---

## 7. 트러블 슈팅 및 이슈 해결과정

* **트러블 슈팅 및 이슈 해결**
  - [JavaMailSender 자동 빈 등록 실패 → 수동 Bean 등록으로 해결](https://velog.io/@hanjyeong/Spring-Data-Jpa-JavamailSender-%EB%B9%88-%EC%83%9D%EC%84%B1-%EC%98%A4%EB%A5%98)
  - [메서드 이름 규칙 불일치로 발생한 ClassCastException 해결](https://velog.io/@hanjyeong/QueryTypeMismatchExceptionjpa-%EB%A9%94%EC%84%9C%EB%93%9C-%EC%9D%B4%EB%A6%84-%EA%B7%9C%EC%B9%99)
  - **트랜잭션 이슈**: EmailToken 생성 시점과 DB 반영 시점 불일치 문제 해결
  - **참조 무결성 오류**: 회원 탈퇴 시 연관 데이터 삭제 정책(Cascade/OrphanRemoval) 수정
 
* **운영 안정화 및 성능 최적화**
    - [SpringScheduler에서 Redis로 바꾸기](https://velog.io/@hanjyeong/SpringSchedeler%EC%99%80-Redis)
    - **API Rate Limiting 도입**: Bucket4j 선정 이유, RateLimite를 설정한 이유 

---

## 8. 팀 구성
| 구분 | 성명 |
|:---:|:---|
| **BE (Web/Mobile)** | 김지오, 남궁다연, 방혁, 한지형 |
| **Design** | 이보영 |
| **FE (Web)** | 이동수, 박성재, 노경미, 김수민 |
| **FE (Mobile)** | 정우창, 유지석, 이수빈 |

