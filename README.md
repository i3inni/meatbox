![header](https://capsule-render.vercel.app/api?type=rect&color=auto&height=250&section=header&text=Meatbox%20(Clone)&fontSize=70)

> Java Servlet/JSP 기반 정육 전문 이커머스 클론 코딩 (팀 스터디)

<br>

## :open_book: 목차
- [프로젝트 소개](#프로젝트-소개)
- [👤 저의 기여](#-저의-기여)
- [🛠️ 기술 스택](#-기술-스택)
- [📁 프로젝트 구조](#-프로젝트-구조)
- [⚙️ 실행 방법](#-실행-방법)

<br>

<a id="프로젝트-소개"></a>
## 📋 프로젝트 소개

**meatbox (클론 코딩)** 는 Java Servlet/JSP와 Model 2 MVC 아키텍처 학습을 목적으로 진행한 **팀 스터디** 프로젝트입니다. 기존에 운영 중인 정육 전문 이커머스 웹 애플리케이션을 클론 코딩하며 백엔드 웹 개발의 전반적인 흐름을 익혔습니다.

### 🚀 주요 기능
- **회원 관리:** 일반 회원 및 판매자 회원가입, 로그인, 로그아웃
- **상품 관리:** 상품 목록 조회, 상품 상세 페이지, 판매자 상품 등록
- **주문 관리:** 장바구니 추가/조회/삭제, 상품 주문(바로 구매/장바구니 구매), 결제
- **관리자(BO):** 판매자 상품 등록 요청 승인 및 관리

<br>

<a id="-저의-기여"></a>
## 👤 저의 기여

저는 이 프로젝트에서 **사용자 인증 및 주문 핵심 로직**의 백엔드 개발을 담당했습니다.

* **로그인 기능:** `LoginController` 및 `LoginAction`을 구현하여 사용자 인증 로직을 처리하고 세션을 관리했습니다.
* **장바구니 기능:** `CartController`를 통해 장바구니 상품 추가, 삭제, 조회 기능을 구현했습니다.
* **주문 관리:** `OrderController`를 설계하여, '바로 구매' 및 '장바구니 구매' 시 주문 페이지로 상품 정보를 전달하고, 최종 주문을 처리하는 로직을 담당했습니다.

<br>

<a id="-기술-스택"></a>
## 🛠️ 기술 스택

| 구분 | 기술 |
|------|------|
| **Backend** | ![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white) ![JSP/Servlet](https://img.shields.io/badge/JSP/Servlet-E95420?style=for-the-badge&logo=apachetomcat&logoColor=white) |
| **Database** | ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white) (JDBC) |
| **Server** | ![Apache Tomcat](https://img.shields.io/badge/Apache_Tomcat-F8DC75?style=for-the-badge&logo=apachetomcat&logoColor=black) |

<br>

<a id="-프로젝트-구조"></a>
## 📁 프로젝트 구조
```bash
ROOT/
├── src/main/java/
│   ├── com/
│   │   ├── Action.java           # MVC 패턴의 Action 인터페이스
│   │   ├── ActionForward.java    # 포워딩 정보 객체
│   │   ├── cart/
│   │   │   ├── action/           # 장바구니 비즈니스 로직
│   │   │   └── controller/       # CartController.java
│   │   ├── login/
│   │   │   ├── action/           # 로그인 비즈니스 로직
│   │   │   └── controller/       # LoginController.java
│   │   ├── order/
│   │   │   └── controller/       # OrderController.java
│   │   ├── product/
│   │   │   ├── action/
│   │   │   └── controller/       # ProductController.java
│   │   └── register/
│   │       ├── action/
│   │       └── controller/       # RegisterController.java
│   └── jdbc/
└── src/main/webapp/
    ├── WEB-INF/
    │   └── web.xml               # 서블릿 매핑
    ├── cart/                     # 장바구니 JSP
    ├── include/                  # 헤더/푸터
    ├── login/                    # 로그인 JSP
    ├── order/                    # 주문 JSP
    ├── product/                  # 상품 JSP
    ├── register/                 # 회원가입 JSP
    └── www.meatbox.co.kr/ (home.jsp) # 메인 페이지
