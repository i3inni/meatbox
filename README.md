네, 요청하신대로 각 레포지토리의 README.md 파일을 생성해 드립니다.사용자님의 이전 설명을 바탕으로 [팀 스터디] 와 **[해커톤]**을 구분하고, 각 프로젝트에서 담당하신 역할(기여) 을 명시하여 작성했습니다.1. meatboxJava Servlet/JSP 기반 정육 전문 이커머스 클론 코딩 (팀 스터디):open_book: 목차프로젝트 소개👤 저의 기여🛠️ 기술 스택📁 프로젝트 구조⚙️ 실행 방법<a id="프로젝트-소개"></a>📋 프로젝트 소개meatbox (클론 코딩) 는 Java Servlet/JSP와 Model 2 MVC 아키텍처 학습을 목적으로 진행한 팀 스터디 프로젝트입니다. 기존에 운영 중인 정육 전문 이커머스 웹 애플리케이션을 클론 코딩하며 백엔드 웹 개발의 전반적인 흐름을 익혔습니다.🚀 주요 기능회원 관리: 일반 회원 및 판매자 회원가입, 로그인, 로그아웃상품 관리: 상품 목록 조회, 상품 상세 페이지, 판매자 상품 등록주문 관리: 장바구니 추가/조회/삭제, 상품 주문(바로 구매/장바구니 구매), 결제관리자(BO): 판매자 상품 등록 요청 승인 및 관리<a id="-저의-기여"></a>👤 저의 기여저는 이 프로젝트에서 사용자 인증 및 주문 핵심 로직의 백엔드 개발을 담당했습니다.로그인 기능: LoginController 및 LoginAction을 구현하여 사용자 인증 로직을 처리하고 세션을 관리했습니다.장바구니 기능: CartController를 통해 장바구니 상품 추가, 삭제, 조회 기능을 구현했습니다.주문 관리: OrderController를 설계하여, '바로 구매' 및 '장바구니 구매' 시 주문 페이지로 상품 정보를 전달하고, 최종 주문을 처리하는 로직을 담당했습니다.<a id="-기술-스택"></a>🛠️ 기술 스택구분기술BackendDatabase(JDBC)Server<a id="-프로젝트-구조"></a>📁 프로젝트 구조BashROOT/
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
<a id="-실행-방법"></a>⚙️ 실행 방법MySQL 데이터베이스에 스키마 및 테이블을 생성합니다.jdbc.db.connection.DBConnectionManager 클래스의 DB 연결 정보(URL, user, password)를 수정합니다.프로젝트를 .war 파일로 빌드합니다.Apache Tomcat 서버에 .war 파일을 배포(deploy)한 후 서버를 실행합니다.
