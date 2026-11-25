# Ustaad360 | Full-Stack Service Marketplace
### System Architecture & Design Documentation

> **Note**
> This repository serves as the official architectural documentation and system design reference for **Ustaad360**, my undergraduate capstone project. The complete application source code remains private to protect intellectual property and business logic. This repository showcases the system architecture, design decisions, technology stack, and software engineering practices behind the project.

---

![.NET](https://img.shields.io/badge/.NET-9.0-purple)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET-Core-blue)
![React](https://img.shields.io/badge/React-19-61DAFB)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-336791)
![React Native](https://img.shields.io/badge/Mobile-React%20Native-61DAFB)

## Overview

**Ustaad360** is a full-stack service marketplace developed as my undergraduate capstone project for the Bachelor of Science in Computer Science.

The platform connects customers with verified technicians for home and business services while addressing one of the most significant challenges in service marketplaces: **trust**.

Rather than focusing only on service booking, Ustaad360 was designed around dependable software engineering principles, including secure authentication, role-based authorization, escrow-oriented payment workflows, real-time communication, transparent dispute management, and Clean Architecture intended to support maintainability and testability.

Developing Ustaad360 strengthened my interest in advanced software systems and directly inspired my research interests in:

- Dependable Distributed Systems
- Cloud-Native Computing
- Microservices Architecture
- Fault-Tolerant Software Systems
- AI for Systems (AI4Systems)
- Trust Management in Distributed Platforms

These research interests form the foundation of my graduate studies and research proposals for the **Institute of Science Tokyo (Japan)** and **KAIST – Kim Jaechul Graduate School of AI (South Korea)**.

---

## System Architecture

The platform follows **Clean Architecture**, separating business logic from infrastructure and presentation layers to maximize maintainability, scalability, testability, and long-term extensibility.

```mermaid
flowchart LR
    subgraph Clients
        WEB[React Web App]
        MOBILE[React Native App]
    end

    subgraph Presentation
        API[ASP.NET Core Web API]
        HUBS[SignalR Hubs]
    end

    subgraph Application
        APP[Use Cases and Application Services]
    end

    subgraph Domain
        DOMAIN[Entities and Business Rules]
    end

    subgraph Infrastructure
        INFRA[Persistence and Integrations]
        DB[(PostgreSQL)]
        EXT[External Services]
    end

    WEB --> API
    MOBILE --> API
    API --> APP
    API --> HUBS
    HUBS --> APP
    APP --> DOMAIN
    INFRA --> APP
    INFRA --> DOMAIN
    INFRA --> DB
    INFRA --> EXT
```

### Architecture Principles

- Clean Architecture
- Dependency Injection
- SOLID Principles
- Repository Pattern
- Service-Oriented Design
- Modular Backend Components

---

## Technology Stack

### Backend

- ASP.NET Core Web API
- C#
- Entity Framework Core
- PostgreSQL

### Frontend

- React
- React Native
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

## Core Features

### Authentication

- User Registration
- Login
- JWT Authentication
- Refresh Tokens
- Password Hashing
- Secure Authorization

---

### Role-Based Access

- Customer
- Technician
- Administrator

Each role has dedicated authorization policies and protected endpoints.

---

### Technician Verification

Technicians can:

- Upload documents
- Complete profiles
- Submit verification requests

Administrators review and approve technician accounts before allowing service requests.

---

### Service Marketplace

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

### Trust-Oriented Design

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

### Real-Time Features

SignalR enables:

- Instant notifications
- Live messaging
- Job updates
- Status synchronization

---

### Administrative Dashboard

Administrators can:

- Manage users
- Verify technicians
- Review reports
- Moderate platform activity
- Monitor system operations

---

## Project Structure

```
src/
  Ustaad360.API/            REST API, SignalR hubs, middleware
  Ustaad360.Application/    Use cases, DTOs, validation, contracts
  Ustaad360.Domain/         Entities, domain events, business rules
  Ustaad360.Infrastructure/ EF Core, PostgreSQL, external integrations
```

---

## Engineering Practices

This project demonstrates practical experience with:

- Backend System Design
- REST API Development
- Clean Architecture
- Authentication & Authorization
- Entity Framework Core
- PostgreSQL
- SignalR
- Cloud-Native Development
- Docker
- Dependency Injection
- Software Design Principles
- API and integration testing

---

## Research Motivation

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

## About the Author

**Mukhtiar Shah**

Full-Stack Software Engineer | Backend Systems & Distributed Computing

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
