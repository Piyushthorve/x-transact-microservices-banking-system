# X-Transact: Microservices-Based Banking System

A scalable banking system built using microservices architecture with Spring Boot and Spring Cloud, supporting Accounts, Cards, and Loans services.

## 🚀 Features
- Microservices architecture with independent services
- API Gateway for centralized routing
- Service discovery using Eureka
- Centralized configuration using Config Server
- Secure authentication using Keycloak (JWT)
- Asynchronous communication using Kafka
- Rate limiting using Redis
- Inter-service communication using OpenFeign
- Containerization using Docker

## 🏗️ Architecture
- API Gateway → routes requests
- Eureka → service discovery
- Config Server → centralized config
- Microservices → business logic
- Kafka → async communication
- Redis → rate limiting

## 🛠️ Tech Stack
- Backend: Spring Boot, Spring Cloud
- Security: Keycloak, JWT
- Messaging: Kafka
- Cache: Redis
- DevOps: Docker, Kubernetes
- Database: H2

## ▶️ How to Run
1. Start Config Server
2. Start Eureka Server
3. Start all microservices
4. Start API Gateway
5. Access APIs via Gateway

## 📌 Future Improvements
- Add persistent DB (MySQL/Postgres)
- Implement distributed tracing (Zipkin)
- Add monitoring dashboard


## 🏗️ Architecture Diagram

```mermaid
flowchart TB

%% ===== CLIENT LAYER =====
A[Client / Frontend App]

%% ===== GATEWAY =====
B[API Gateway]

%% ===== MICROSERVICES =====
subgraph Services
    C[Accounts Service]
    D[Cards Service]
    E[Loans Service]
end

%% ===== INFRA =====
subgraph Infrastructure
    F[Eureka Server]
    G[Config Server]
    H[Message Service]
end

%% ===== DATABASES =====
subgraph Databases
    DB1[(Accounts DB)]
    DB2[(Cards DB)]
    DB3[(Loans DB)]
end

%% ===== FLOW =====
A --> B

B --> C
B --> D
B --> E

%% Service to DB
C --> DB1
D --> DB2
E --> DB3

%% Service to Messaging
C --> H
D --> H
E --> H

%% Service Discovery
C --> F
D --> F
E --> F
B --> F

%% Config Server
C --> G
D --> G
E --> G
B --> G

%% ===== STYLING =====
classDef gateway fill:#fff3e0,stroke:#fb8c00,stroke-width:1px;
classDef service fill:#e3f2fd,stroke:#1e88e5,stroke-width:1px;
classDef infra fill:#ede7f6,stroke:#5e35b1,stroke-width:1px;
classDef db fill:#f1f8e9,stroke:#7cb342,stroke-width:1px;

class B gateway;
class C,D,E service;
class F,G,H infra;
class DB1,DB2,DB3 db;

