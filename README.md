<div align="center">

# Spring Boot RabbitMQ Server

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1200&color=FF6B35&center=true&vCenter=true&width=900&lines=Spring+Boot+RabbitMQ+Server;Event-Driven+Architecture;Asynchronous+Messaging;Producer+%E2%86%94+RabbitMQ+%E2%86%94+Consumer" alt="Typing SVG" />

<br>

[![Java](https://img.shields.io/badge/Java-17-orange?style=for-the-badge&logo=openjdk)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.5-green?style=for-the-badge&logo=springboot)](https://spring.io/projects/spring-boot)
[![RabbitMQ](https://img.shields.io/badge/RabbitMQ-3-orange?style=for-the-badge&logo=rabbitmq)](https://www.rabbitmq.com/)
[![Maven](https://img.shields.io/badge/Maven-Build-red?style=for-the-badge&logo=apachemaven)](https://maven.apache.org/)
[![REST API](https://img.shields.io/badge/API-REST-blue?style=for-the-badge)]()

---

### Production-ready Spring Boot application demonstrating asynchronous messaging using RabbitMQ and Event-Driven Architecture.

</div>

---

# Overview

This project demonstrates how distributed applications communicate asynchronously using **RabbitMQ**.

Instead of tightly coupling services, the application publishes messages to RabbitMQ where consumers process them independently. This architecture improves scalability, resiliency, and overall system performance.

---

# Features

- Spring Boot
- RabbitMQ Producer
- RabbitMQ Consumer
- Asynchronous Message Processing
- REST APIs
- Event-Driven Architecture

---

# Tech Stack

Java 21 -> Programming Language
Spring Boot -> Backend Framework
RabbitMQ -> Message Broker
Spring AMQP -> RabbitMQ Integration
REST API -> API Layer
Maven -> Dependency Management

---

# 🏛Architecture

```mermaid
flowchart LR

A(Client)
B(Spring Boot REST API)
C(Message Producer)
D(RabbitMQ Exchange)
E(Queue)
F(Message Consumer)

A --> B
B --> C
C --> D
D --> E
E --> F
```

---

# 🔄 Message Flow

```mermaid
sequenceDiagram

Client->>REST API: POST /publish
REST API->>Producer: Publish Message
Producer->>RabbitMQ: Send Event
RabbitMQ->>Consumer: Deliver Event
Consumer-->>Consumer: Process Message
```

---

# Project Structure

```
springboot-rabbitmq-server
│
├── src
│   ├── main
│   │   ├── java
│   │   │   ├── config
│   │   │   ├── controller
│   │   │   ├── producer
│   │   │   ├── consumer
│   │   │   ├── dto
│   │   │   └── SpringbootRabbitmqApplication.java
│   │   │
│   │   └── resources
│   │       └── application.properties
│   │
│   └── test
│
├── pom.xml
└── README.md
```

---

# Getting Started

## Clone Repository

```bash
git clone https://github.com/sonaltamse/rabbitmq-event-processor.git

cd rabbitmq-event-processor
```

---

## Start RabbitMQ

Using Docker

```bash
docker run -d \
--hostname rabbitmq \
--name rabbitmq \
-p 5672:5672 \
-p 15672:15672 \
rabbitmq:3-management
```

RabbitMQ Dashboard

```
http://localhost:15672
```

Default Credentials

```
Username : guest
Password : guest
```

---

## Run the Project

```bash
mvn spring-boot:run
```

or

```bash
./mvnw spring-boot:run
```

---

# ⚙ Configuration

```properties
spring.rabbitmq.host=localhost
spring.rabbitmq.port=5672
spring.rabbitmq.username=guest
spring.rabbitmq.password=guest
```
---

# Why RabbitMQ?

RabbitMQ enables applications to communicate asynchronously by acting as a reliable message broker.

Benefits include:

- Faster response times
- Loose coupling between services
- Improved scalability
- Better fault tolerance
- Event-driven communication

---
<div align="center">

### Made using Spring Boot & RabbitMQ

**Happy Coding!**

</div>
