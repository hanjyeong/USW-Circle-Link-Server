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

- **이메일 전송 기반 인증 기능 구현**
    - Spring Mail을 활용한 이메일 발송 로직 구현
    - 인증 코드 생성 및 만료 시간 관리
    - Redis를 이용해 인증 코드 저장 및 TTL(Time To Live) 설정
    - 회원가입, 아이디/비밀번호 찾기, 회원 탈퇴 등 인증 흐름 설계 및 구현 
- **API 요청 횟수 제한(Rate Limiting)**
    - Bucket4j 라이브러리를 적용하여 API별 요청 횟수 제한
    - Redis 기반 분산 환경에서도 동작 가능하도록 설계 및 구현
- **DTO 입력값 검증 구조 설계**
    - ValidationGroup을 활용하여 API 상황별 유효성 검사 분리
    - 요청 목적에 따라 필요한 필드만 검증하도록 설계 및 구현
- **Enum 필드값 유효성 검사**
    - 커스텀 Validator 및 어노테이션 구현
    - 잘못된 Enum 값 요청에 대한 사전 차단 로직 적용

---

## 7. 트러블 슈팅 및 이슈 해결과정
  - [JavaMailSender 자동 빈 등록 실패 → 수동 Bean 등록으로 해결](https://velog.io/@hanjyeong/Spring-Data-Jpa-JavamailSender-%EB%B9%88-%EC%83%9D%EC%84%B1-%EC%98%A4%EB%A5%98)
  - [메서드 이름 규칙 불일치로 발생한 ClassCastException 해결](https://velog.io/@hanjyeong/QueryTypeMismatchExceptionjpa-%EB%A9%94%EC%84%9C%EB%93%9C-%EC%9D%B4%EB%A6%84-%EA%B7%9C%EC%B9%99)
  - [트랜잭션 전파(REQUIRED)로 하위 변경이 상위 롤백에 묶인 문제 해결](https://velog.io/@hanjyeong/Spring-%ED%8A%B8%EB%9E%9C%EC%9E%AD%EC%85%98%EC%9D%98-%EC%A4%91%EC%B2%A9%EC%9C%BC%EB%A1%9C-%EC%9D%B8%ED%95%9C-%EB%AC%B8%EC%A0%9C)
  - [SpringScheduler에서 Redis로 바꾸기](https://velog.io/@hanjyeong/%ED%9A%8C%EC%9B%90%EA%B0%80%EC%9E%85%EA%B3%BC-%EA%B4%80%EB%A0%A8%EB%90%9C-%EA%B8%B0%EB%B3%B8-%EB%8F%84%EB%A9%94%EC%9D%B8-%EC%88%98%EC%A0%95%ED%95%98%EA%B8%B0)
  - [API별 Rate Limiting 도입하기- Bucket4j](https://velog.io/@hanjyeong/Bucket4j%EB%A5%BC-%EC%9D%B4%EC%9A%A9%ED%95%98%EC%97%AC-RateLimite-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0)
  - [Dto 검증을 위한 ValidationGroup 설정하기](https://velog.io/@hanjyeong/Valid%EC%99%80-Validated-%EC%B0%A8%EC%9D%B4-Dto-%EC%9C%A0%ED%9A%A8%EC%84%B1-%EA%B2%80%EC%A6%9D-%EC%88%9C%EC%84%9C-%EC%A7%80%EC%A0%95%ED%95%98%EA%B8%B0) 

---

## 8. 팀 구성
| 구분 | 성명 |
|:---:|:---|
| **BE (Web/Mobile)** | 김지오, 남궁다연, 방혁, 한지형 |
| **Design** | 이보영 |
| **FE (Web)** | 이동수, 박성재, 노경미, 김수민 |
| **FE (Mobile)** | 정우창, 유지석, 이수빈 |

