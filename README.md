# Ustaad360 Backend

> A cloud-native backend platform for a trust-aware technician marketplace built with ASP.NET Core, Clean Architecture, and modern backend engineering practices.

![.NET](https://img.shields.io/badge/.NET-9.0-purple)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET-Core-blue)
![SQL Server](https://img.shields.io/badge/Database-SQL%20Server-red)
![License](https://img.shields.io/badge/License-MIT-green)

---

## Overview

Ustaad360 is my undergraduate capstone project developed as part of my Bachelor of Science in Computer Science.

The platform connects customers with verified technicians for home and business services while addressing one of the biggest challenges in local service marketplaces—**trust**.

Instead of focusing solely on booking services, the system was designed around dependable workflows including secure authentication, role-based authorization, escrow-oriented payment processing, document verification, real-time communication, and transparent dispute handling.

Developing Ustaad360 motivated my research interests in:

- Dependable Distributed Systems
- Cloud-Native Computing
- Fault-Tolerant Software Systems
- AI for Systems (AI4Systems)
- Trust Management in Digital Platforms

These research interests form the basis of my graduate school applications to KAIST (South Korea) and the Institute of Science Tokyo (Japan).

---

# Architecture

The backend follows **Clean Architecture**, separating business rules from infrastructure to improve maintainability, scalability, and testability.

```
Presentation Layer
        │
ASP.NET Core Web API
        │
Application Layer
(Business Logic)
        │
Domain Layer
(Entities & Rules)
        │
Infrastructure Layer
(Database, Authentication, External Services)
```

### Architecture Principles

- Clean Architecture
- Dependency Injection
- SOLID Principles
- Repository Pattern
- Service-Oriented Design
- Modular Backend Components

---

# Technology Stack

### Backend

- ASP.NET Core Web API
- C#
- Entity Framework Core
- SQL Server

### Frontend

- React
- TypeScript

### Authentication & Security

- JWT Authentication
- Role-Based Access Control (RBAC)
- Refresh Tokens
- Authorization Policies

### Real-Time Communication

- SignalR

### Cloud & DevOps

- Docker
- Git
- GitHub

### API Documentation

- Swagger / OpenAPI

---

# Core Features

## Authentication

- User Registration
- Login
- JWT Authentication
- Refresh Tokens
- Password Hashing
- Secure Authorization

---

## Role-Based Access

- Customer
- Technician
- Administrator

Each role has dedicated authorization policies and protected endpoints.

---

## Technician Verification

Technicians can:

- Upload documents
- Complete profiles
- Submit verification requests

Administrators review and approve technician accounts before allowing service requests.

---

## Service Marketplace

Customers can:

- Browse services
- View technician profiles
- Create service requests
- Track job progress
- Review completed work

Technicians can:

- Accept jobs
- Manage requests
- Update job status
- Complete services

---

## Trust-Oriented Design

The platform was designed around trust rather than simple booking functionality.

Implemented mechanisms include:

- Escrow-inspired payment workflow
- Identity verification
- Role separation
- Transparent service lifecycle
- Review system
- Secure communication

These ideas later motivated my graduate research interests in dependable distributed systems and trustworthy cloud infrastructure.

---

## Real-Time Features

SignalR enables:

- Instant notifications
- Live messaging
- Job updates
- Status synchronization

---

## Administrative Dashboard

Administrators can:

- Manage users
- Verify technicians
- Review reports
- Moderate platform activity
- Monitor system operations

---

# Project Structure

```
src/

API/
Presentation Layer

Application/
Business Logic
CQRS
Services

Domain/
Entities
Interfaces
Business Rules

Infrastructure/
Entity Framework Core
Authentication
Persistence
External Services
```

---

# Skills Demonstrated

This project demonstrates practical experience with:

- Backend System Design
- REST API Development
- Clean Architecture
- Authentication & Authorization
- Entity Framework Core
- SQL Server
- SignalR
- Cloud-Native Development
- Docker
- Dependency Injection
- Software Design Principles
- Production API Development

---

# Research Motivation

Although Ustaad360 solves many trust-related challenges through authentication, authorization, and secure workflows, developing the platform exposed several research questions that cannot be addressed solely at the application layer.

Examples include:

- Detecting fraudulent user behavior
- Maintaining trust under distributed failures
- Intelligent anomaly detection
- Fault-tolerant cloud services
- Adaptive trust management
- Reliable distributed architectures

These challenges inspired my proposed graduate research in:

- Dependable Distributed Systems
- AI for Systems
- Cloud Computing
- Intelligent Cloud Infrastructure
- Fault-Tolerant Software Systems

---

# Future Improvements

Planned research-driven enhancements include:

- AI-assisted anomaly detection
- Distributed trust scoring
- Kubernetes deployment
- OpenTelemetry observability
- Prometheus & Grafana monitoring
- Redis caching
- RabbitMQ event-driven messaging
- Distributed tracing
- Cloud-native scalability
- Microservices architecture

---

# About the Author

**Mukhtiar Shah**

Backend Software Engineer | Distributed Systems & Cloud Computing Research Applicant

Research Interests:

- Dependable Distributed Systems
- Cloud Computing
- AI for Systems (AI4Systems)
- Fault-Tolerant Computing
- Cloud-Native Applications
- Backend Engineering

GitHub:
https://github.com/MUKHTIARSHAH

LinkedIn:
https://linkedin.com/in/mukhtiar-shah-4567221aa

Email:
shahsaib256@gmail.com

---

# License

This project is released under the MIT License.
