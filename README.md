# NestJS MSA Project

**NestJS 기반 마이크로서비스 아키텍처(MSA) 프로젝트**  
API Gateway, 서비스 분리, 동기/비동기 통신, Docker/Docker Compose, Postgres 연동까지 실습하며  
NestJS에서의 MSA 구조를 학습하고 구현하는 프로젝트입니다.  

---

## 프로젝트 개요
- **모놀리스 vs 마이크로서비스** 개념 비교 및 MSA 도입 이유 이해
- **API Gateway**를 통한 클라이언트 요청 라우팅
- **마이크로서비스 분리**: 인증, 게시판, 결제 등 (예시)
- **동기 통신**: TCP / HTTP 기반 서비스 간 호출
- **비동기 통신**: Kafka를 이용한 이벤트 기반 아키텍처
- **Docker & Docker Compose**를 활용한 로컬 개발 환경 구성
- **Postgres** 데이터베이스 연동

---

## 기술 스택
- **Framework**: NestJS (Node.js 기반)  
- **Language**: TypeScript  
- **Container**: Docker, Docker Compose  
- **Database**: PostgreSQL  
- **Messaging**: Kafka  
- **Architecture**: API Gateway + Microservices  

---

## 프로젝트 구조 (예시)

```bash
nestjs-msa/
├── api-gateway/             # API Gateway
├── services/
│   ├── auth-service/        # 인증 서비스
│   ├── board-service/       # 게시판 서비스
│   └── payment-service/     # 결제 서비스
├── docker-compose.yml
├── kafka/                   # Kafka 설정
├── postgres/                # Postgres 설정
└── README.md



# 의존성 설치
pnpm install

# 개별 서비스 실행 (예: auth-service)
cd services/auth-service
pnpm start:dev

# Docker Compose로 전체 마이크로서비스 실행
docker-compose up --build


## 향후 개선 방향
- 서비스 간 인증/인가 체계 강화 (JWT, OAuth)  
- 모니터링/로깅 시스템 (ELK Stack, Prometheus, Grafana) 적용  
- 서비스 확장 (주문, 알림, 채팅 등)  
- CI/CD 파이프라인 구축 (Vercel, GitHub Actions, Kubernetes)  
