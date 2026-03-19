# **X-Transact: Microservices-Based Banking Application**  

X-Transact is a comprehensive banking application designed to demonstrate the implementation of a **microservices architecture** using **Spring Boot**. The project encompasses distinct services for managing **loans, cards, and accounts** while integrating advanced features such as **containerization, message-driven solutions with Kafka, and monitoring tools** including **Prometheus, Grafana, Loki, and Promtail**. Additionally, the application is orchestrated using **Kubernetes** for efficient deployment and scalability.  

## **Features**  

- **Accounts Microservice**: Manages customer account information and related operations.  
- **Cards Microservice**: Handles credit and debit card services, including issuance and management.  
- **Loans Microservice**: Oversees loan products, applications, and processing.  
- **Configuration Server**: Centralized configuration management for all microservices.  
- **Eureka Server**: Service discovery to facilitate communication between microservices.  
- **Gateway Server**: API gateway that routes requests to the appropriate microservices.  
- **Message Broker**: Implements Apache Kafka for asynchronous communication between services.  
- **Monitoring and Logging**: Integrates Prometheus and Grafana for monitoring, and Loki with Promtail for logging.  
- **Containerization and Orchestration**: Utilizes Docker for containerization and Kubernetes for orchestration and management.  

## **Prerequisites**  

Before setting up the application, ensure you have the following installed:  

- Java Development Kit (JDK) 11 or higher  
- Docker  
- Kubernetes  
- Apache Kafka  
- Prometheus  
- Grafana  
- Loki  
- Promtail  

## **Getting Started**  

### **1. Clone the Repository**  

```bash
git clone https://github.com/Aaditatgithub/X-Transact.git
cd X-Transact
```

### **2. Build the Microservices**  

Navigate to each microservice directory (`accounts`, `cards`, `loans`, etc.) and build them using Maven:  

```bash
mvn clean install
```

### **3. Start the Infrastructure Services**  

Use Docker Compose to start the **Configuration Server, Eureka Server, and Gateway Server**:  

```bash
docker-compose up -d
```

### **4. Deploy Microservices to Kubernetes**  

Apply the Kubernetes deployment files located in the `k8s` directory:  

```bash
kubectl apply -f k8s/
```

### **5. Set Up Monitoring and Logging**  

Configure **Prometheus, Grafana, Loki, and Promtail** using the provided configuration files in the `monitoring` directory.  

### **6. Access the Application**  

The application can be accessed via the **API Gateway**. Ensure that all services are up and running, then use the gateway's endpoint to interact with the microservices.  

---

This project was developed as a **learning exercise** to explore **microservices architecture** using **Spring Boot** and associated technologies.  
