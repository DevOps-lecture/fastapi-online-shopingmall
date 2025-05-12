# fastapi-online-shopingmall

프로젝트 개요: 온라인 쇼핑몰 API 플랫폼
본 프로젝트는 Java 개발자가 Python FastAPI를 사용하여 구현한 전자상거래 API 시스템입니다. </br>
이 API는 제품 관리, 사용자 인증, 장바구니, 주문 처리, 결제 시스템을 포함하는 완전한 쇼핑몰 백엔드 서비스를 제공합니다. </br>

## [기술 스택]

언어: Python 3.9+ </br>
웹 프레임워크: FastAPI </br>
ORM: SQLAlchemy </br>
데이터베이스: PostgreSQL </br>
인증: JWT(JSON Web Tokens) </br>
문서화: Swagger/OpenAPI </br>
테스트: pytest </br>
배포: Docker, GitHub Actions, AWS </br>

## [주요 기능] </br>

1. 사용자 관리 및 인증 </br>

회원가입 및 로그인 </br>
JWT 기반 인증 </br>
사용자 프로필 관리 </br>
역할 기반 권한 제어 (관리자, 일반 사용자) </br>

2. 제품 관리 </br>

카테고리별 제품 조회 </br>
제품 상세 정보 </br>
제품 검색 및 필터링 </br>
재고 관리 </br>

3. 장바구니 </br>

장바구니 항목 추가/수정/삭제 </br>
장바구니 조회 </br>
장바구니 상태 관리 </br>

4. 주문 관리 </br>

주문 생성 및 조회 </br>
주문 상태 관리 </br>
주문 이력 </br>

5. 결제 처리 </br>

결제 수단 등록 </br>
결제 처리 </br>
결제 내역 조회 </br>

6. 관리자 기능 </br>

제품 추가/수정/삭제 </br>
사용자 관리 </br>
주문 상태 변경 </br>
매출 보고서 </br>

