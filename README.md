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

## 🏗️ Architecture Diagram

```mermaid
flowchart LR

%% Client Layer
A[Client / Frontend App]

%% Gateway
B[API Gateway]

%% Service Discovery
C[Eureka Server]

%% Config Server
D[Config Server]

%% Microservices
E[Accounts Service]
F[Cards Service]
G[Loans Service]
H[Message Service]

%% Database Layer
DB1[(Accounts DB)]
DB2[(Cards DB)]
DB3[(Loans DB)]

%% Connections

A --> B

B --> E
B --> F
B --> G

E --> DB1
F --> DB2
G --> DB3

E --> H
F --> H
G --> H

%% Infra connections
E --> C
F --> C
G --> C
B --> C

E --> D
F --> D
G --> D
B --> D

%% Styling
classDef service fill:#e3f2fd,stroke:#1e88e5,stroke-width:1px;
classDef infra fill:#fff3e0,stroke:#fb8c00,stroke-width:1px;

class E,F,G,H service;
class B,C,D infra;

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
