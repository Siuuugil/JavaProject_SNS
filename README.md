# JavaProject_SNS (Clonestagram)

> Spring Boot 기반 인스타그램 클론 SNS 웹 애플리케이션

**유한대학교 Java 팀 프로젝트** | 팀 프로젝트 | [원본 팀 레포지토리 →](https://github.com/Seungho1201/JavaProject_SNS)

---

## 📋 목차

- [소개](#소개)
- [🙋 본인 담당 파트](#-본인-담당-파트)
- [주요 기능](#주요-기능)
- [기술 스택](#기술-스택)
- [설치 및 실행](#설치-및-실행)

---

## 소개

인스타그램의 핵심 기능을 클론한 SNS 웹 애플리케이션입니다.  
게시글 작성, 좋아요, 댓글, 스크랩 등 SNS의 기본 기능을 Spring Boot로 구현했습니다.

---

## 🙋 본인 담당 파트

### 👤 팀원 역할 분담

| 이름 | 역할 |
| :---: | :---: |
| 김수길 | <b>팀장</b>,  글 작성 및 수정 구현|
| 김용빈 | 마이 페이지 구현 |
| 오승호 | 메인 페이지, 로그인 및 회원가입, 비동기 처리, DB 구현 |


---

### 📝 게시글 (Post)

Spring Boot MVC 패턴으로 게시글의 전체 흐름을 구현했습니다.

**구현 내용**
- 게시글 작성 / 수정 / 삭제 (본인 게시글만 수정·삭제 가능하도록 작성자 검증 처리)
- 게시글 작성 시 이미지 파일 첨부 기능 — UUID로 파일명 중복을 방지하여 서버에 저장
- 게시글 삭제 시 연관된 좋아요, 스크랩, 댓글 데이터를 함께 삭제하는 연관 데이터 정리 처리
- 게시글 상세 조회 API (내용, 이미지, 추천 수, 작성일 반환)

---

### ❤️ 좋아요 (Likes)

**구현 내용**
- 게시글 좋아요 등록 및 취소
- 동일 유저가 같은 게시글에 중복 좋아요를 할 수 없도록 중복 검증 처리
- 좋아요 등록 시 게시글의 추천 수 증가, 취소 시 감소 (0 미만으로 내려가지 않도록 처리)

---

### 🔖 스크랩 (Scrap)

**구현 내용**
- 게시글 스크랩 등록 및 취소 (토글 방식)
- 이미 스크랩한 게시글 재요청 시 자동으로 스크랩 취소 처리

---

### 💬 댓글 (Comment)

**구현 내용**
- 게시글에 댓글 작성
- 특정 게시글의 댓글 목록 조회

---

## 주요 기능

- 회원가입 / 로그인 (Spring Security)
- 게시글 작성 / 수정 / 삭제 (이미지 첨부 포함)
- 게시글 좋아요 / 취소
- 게시글 스크랩 / 취소
- 댓글 작성 및 조회
- 마이페이지

---

## 기술 스택

### Backend
| 기술 | 용도 |
|------|------|
| Java | 메인 언어 |
| Spring Boot | 웹 프레임워크 |
| Spring Security | 인증 / 인가 |
| Spring Data JPA | DB 연동 |
| MySQL | 데이터베이스 |

### Frontend
| 기술 | 용도 |
|------|------|
| Thymeleaf | 서버 사이드 템플릿 |
| HTML / CSS / JavaScript | UI 구성 |

---

## 설치 및 실행

1. MySQL에서 데이터베이스 생성
2. `application.properties`에서 DB 연결 정보 설정
3. 프로젝트 빌드 후 실행
4. `http://localhost:8080` 접속

---

# 구현 이미지

로그인 페이지
![Image](https://github.com/user-attachments/assets/a6d3aa17-64ad-4e2f-bc44-5e409d7a1fbc)

회원가입 페이지
![Image](https://github.com/user-attachments/assets/bbfa0465-04bd-4f91-ab4d-73fa9c0d0c7e)

메인 페이지
![Image](https://github.com/user-attachments/assets/56317dec-0349-47a7-8671-f6906cabb62b)

댓글
![Image](https://github.com/user-attachments/assets/7df86110-787c-46d5-ac44-f55cb8e8e1ed)

마이페이지
![Image](https://github.com/user-attachments/assets/dbbd956e-803c-44a0-ac6b-e94a88849124)

게시글 저장 후 마이페이지
![Image](https://github.com/user-attachments/assets/76e7bfab-27a6-4fb2-8419-5166079141af)

---

## 원본 레포지토리

팀 전체 기여 내역은 원본 레포지토리에서 확인할 수 있습니다.  
👉 [https://github.com/Siuuugil/JavaProject_SNS](https://github.com/Seungho1201/JavaProject_SNS)

