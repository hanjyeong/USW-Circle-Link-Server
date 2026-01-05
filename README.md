<p>
  <img width="1024" height="500" alt="image" src="https://github.com/user-attachments/assets/5e9f9dcd-717a-4f33-843b-4a1d985e53b4" />
</p>

- 사이트 : [동구라미 웹페이지에서 보기 ](https://donggurami.net/)
- 앱 스토어: [iOS 앱 스토어에서 보기](https://apps.apple.com/kr/app/%EB%8F%99%EA%B5%AC%EB%9D%BC%EB%AF%B8/id6692607046)

---
### 📌 프로젝트 개요 

- **프로젝트 이름** : 동구라미
- **프로젝트 목적** : 반복적인 동아리 모집과 지원 절차를 간소화하여 수원대학교 학생들이 동아리 활동을 더 편리하게 이용할 수 있도록 하였습니다.

- **프로젝트 기획 배경**

<img width="717" height="403" alt="1764634872708-9e099a3d-9e60-4bc8-aeda-e781d793c57d_2" src="https://github.com/user-attachments/assets/3b28aefd-2e00-411a-bdeb-36e3b59abb15" />
<img width="717" height="403" alt="1764634872708-9e099a3d-9e60-4bc8-aeda-e781d793c57d_3" src="https://github.com/user-attachments/assets/38f50db3-be81-4fce-af2a-a5da7b6b1f92" />
<img width="717" height="403" alt="1764634872708-9e099a3d-9e60-4bc8-aeda-e781d793c57d_4" src="https://github.com/user-attachments/assets/856db597-d0d4-4804-8f2f-787f83276b89" />


---
### 📌 팀 구성 



### BE - web/ mobile, 4명

| 김지오 | 남궁다연 | 방혁 | 한지형 |
|:-----------:|:-----------:|:-----------:|:-----------:|

### Design, 1명
| 이보영 |
|:-----------:|

### FE - web, 4명

| 이동수 | 박성재 | 노경미 | 김수민 |
|:-----------:|:-----------:|:-----------:|:-----------:|

### FE - mobile, 3명

| 정우창 | 유지석 | 이수빈 |
|:-----------:|:-----------:|:-----------:|

--- 
### 📌 실제 서비스 화면 
#### **동아리 지원자**

<p align="center">
  <a href="https://github.com/user-attachments/assets/fea786a1-5138-40c1-a618-fa3a9877cefc">
    <img width="220" alt="메인페이지" src="https://github.com/user-attachments/assets/fea786a1-5138-40c1-a618-fa3a9877cefc" />
  </a>
  <a href="https://github.com/user-attachments/assets/6ec554bb-4bf3-4dd4-8120-453a70543680">
    <img width="220" alt="동아리 지원하기여 인증 코드 저장 및 TTL(Time To Live) 설정
    - 회원가입, 아이디/비밀번호 찾기, 회원 탈퇴 등 인증 로직 구현 
- **API 요청 횟수 제한(Rate Limiting)**
    - Bucket4j 라이브러리를 적용하여 API별 요청 횟수 제한
    - Redis 기반 분산 환경에서도 동작 가능하도록 설계
- **DTO 입력값 검증 구조 설계**
    - ValidationGroup을 활용하여 API 상황별 유효성 검사 분리
    - 요청 목적에 따라 필요한 필드만 검증하도록 설계
- **Enum 필드값 유효성 검사**
    - 커스텀 Validator 및 어노테이션 구현
    - 잘못된 Enum 값 요청에 대한 사전 차단 로직 적용
- **공통 예외 처리 구조 적용**
    - `@ControllerAdvice` 기반 전역 예외 처리
    - Custom Exception 및 공통 에러 응답 포맷 적용



---

### 📌 기술 스택 

### BE

<table>
  <tr>
    <td>언어</td>
    <td>
      <img src="https://img.shields.io/badge/Java-F89820?style=for-the-badge&logo=openjdk&logoColor=white"/> 
    </td>
  </tr>
  
  <tr>
    <td>프레임워크</td>
    <td>
      <img src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white"/> 
      <img src="https://img.shields.io/badge/JPA-59666C?style=for-the-badge&logo=hibernate&logoColor=white"/>
      <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
      <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white"/>
      <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white"/>
      <img src="https://img.shields.io/badge/EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white"/>
      <img src="https://img.shields.io/badge/S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white"/>
      <img src="https://img.shields.io/badge/RDS-527FFF?style=for-the-badge&logo=amazonrds&logoColor=white"/>
      <img src="https://img.shields.io/badge/FCM-FFCA28?style=for-the-badge&logo=firebase&logoColor=black"/>
      <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white"/>
      <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
    </td>
  </tr>
  
  <tr>
    <td>툴</td>
    <td>
      <img src="https://img.shields.io/badge/IntelliJIDEA-000000?style=for-the-badge&logo=intellijidea&logoColor=white"/>
    </td>
  </tr>
  
</table>

* java 17
* springboot 3.3.1

### cooperation 

<table>
  <tr>
    <td>협업</td>
    <td>
      <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white"/>
      <img src="https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github&logoColor=white"/>
    </td>
  </tr>
  
</table>

---
###  📌 프로젝트 시스템 아키텍쳐

<img width="802" height="425" alt="Image" src="https://github.com/user-attachments/assets/af95256c-bc91-4ae6-abc4-9480c33ad63c" />

---
### 📌 ERD






---

### 📌 트러블 슈팅 및 해결과정 

---
### 📌 느낀점 및 회고 
