# fastapi-online-shopingmall

프로젝트 개요: 온라인 쇼핑몰 API 플랫폼
본 프로젝트는 Java 개발자가 Python FastAPI를 사용하여 구현한 전자상거래 API 시스템입니다. 
이 API는 제품 관리, 사용자 인증, 장바구니, 주문 처리, 결제 시스템을 포함하는 완전한 쇼핑몰 백엔드 서비스를 제공합니다.

[기술 스택]
언어: Python 3.9+
웹 프레임워크: FastAPI
ORM: SQLAlchemy
데이터베이스: PostgreSQL
인증: JWT(JSON Web Tokens)
문서화: Swagger/OpenAPI
테스트: pytest
배포: Docker, GitHub Actions, AWS

프로젝트 구조
ecommerce-api/
│
├── app/                            # 애플리케이션 패키지
│   ├── __init__.py
│   ├── main.py                     # FastAPI 인스턴스와 애플리케이션 설정
│   ├── config.py                   # 환경 설정 및 상수
│   ├── dependencies.py             # 의존성 함수
│   │
│   ├── api/                        # API 엔드포인트 패키지
│   │   ├── __init__.py
│   │   ├── api_v1/                 # API 버전 1
│   │   │   ├── __init__.py
│   │   │   ├── router.py           # 메인 라우터
│   │   │   ├── endpoints/          # 각 도메인별 엔드포인트
│   │   │   │   ├── __init__.py
│   │   │   │   ├── users.py
│   │   │   │   ├── products.py
│   │   │   │   ├── carts.py
│   │   │   │   ├── orders.py
│   │   │   │   └── payments.py
│   │
│   ├── models/                     # SQLAlchemy ORM 모델
│   │   ├── __init__.py
│   │   ├── user.py
│   │   ├── product.py
│   │   ├── cart.py
│   │   ├── order.py
│   │   └── payment.py
│   │
│   ├── schemas/                    # Pydantic 스키마 (데이터 검증)
│   │   ├── __init__.py
│   │   ├── user.py
│   │   ├── product.py
│   │   ├── cart.py
│   │   ├── order.py
│   │   └── payment.py
│   │
│   ├── crud/                       # CRUD 작업 함수
│   │   ├── __init__.py
│   │   ├── base.py                 # 기본 CRUD 작업
│   │   ├── user.py
│   │   ├── product.py
│   │   ├── cart.py
│   │   ├── order.py
│   │   └── payment.py
│   │
│   ├── core/                       # 핵심 기능 모듈
│   │   ├── __init__.py
│   │   ├── security.py             # 인증 및 권한 관련
│   │   ├── exceptions.py           # 커스텀 예외 처리
│   │   └── pagination.py           # 페이지네이션 유틸리티
│   │
│   └── db/                         # 데이터베이스 관련
│       ├── __init__.py
│       ├── base.py                 # 기본 설정
│       └── session.py              # 세션 관리
│
├── alembic/                        # 데이터베이스 마이그레이션
│   ├── versions/
│   └── ...
│
├── tests/                          # 테스트 코드
│   ├── __init__.py
│   ├── conftest.py                 # 테스트 설정
│   ├── test_api/                   # API 테스트
│   │   ├── __init__.py
│   │   ├── test_users.py
│   │   ├── test_products.py
│   │   ├── test_carts.py
│   │   ├── test_orders.py
│   │   └── test_payments.py
│   │
│   └── test_services/              # 서비스 로직 테스트
│       ├── __init__.py
│       └── ...
│
├── docker/                         # Docker 설정
│   ├── Dockerfile                  # 애플리케이션 컨테이너
│   └── docker-compose.yml          # 개발 환경 설정
│
├── scripts/                        # 유틸리티 스크립트
│   ├── start.sh
│   └── seed_db.py                  # 초기 데이터 생성
│
├── .env                            # 환경 변수 (gitignore에 추가)
├── .env.example                    # 환경 변수 예시
├── requirements.txt                # 패키지 의존성
├── README.md                       # 프로젝트 문서
└── .gitignore                      # Git 무시 파일

주요 기능
1. 사용자 관리 및 인증

회원가입 및 로그인
JWT 기반 인증
사용자 프로필 관리
역할 기반 권한 제어 (관리자, 일반 사용자)

2. 제품 관리

카테고리별 제품 조회
제품 상세 정보
제품 검색 및 필터링
재고 관리

3. 장바구니

장바구니 항목 추가/수정/삭제
장바구니 조회
장바구니 상태 관리

4. 주문 관리

주문 생성 및 조회
주문 상태 관리
주문 이력

5. 결제 처리

결제 수단 등록
결제 처리
결제 내역 조회

6. 관리자 기능

제품 추가/수정/삭제
사용자 관리
주문 상태 변경
매출 보고서

