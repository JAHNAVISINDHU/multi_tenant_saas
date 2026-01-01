# Multi-Tenant SaaS Platform – Project & Task Management

A production-ready multi-tenant SaaS application where multiple organizations can register, manage teams, create projects, and track tasks with full data isolation, role-based access control, and subscription limits.

---

##  Features

* Multi-tenant architecture with strict data isolation
* JWT-based authentication
* Role-Based Access Control (Super Admin, Tenant Admin, User)
* User management (CRUD)
* Project & Task management
* Subscription plan enforcement
* Audit logging
* Fully Dockerized (Database, Backend, Frontend)
* One-command startup using Docker Compose

---

## 🛠 Tech Stack

* **Backend:** Node.js, Express
* **Frontend:** React
* **Database:** PostgreSQL
* **Authentication:** JWT
* **Authorization:** RBAC
* **Containerization:** Docker, Docker Compose

---

## 📁 Project Structure

```
project-root/
├── backend/
├── frontend/
├── database/
│   └── init/
│       └── init.sql
├── docs/
│   ├── research.md
│   ├── PRD.md
│   ├── architecture.md
│   └── technical-spec.md
├── docker-compose.yml
└── README.md
```

---

##  Running the Application (MANDATORY)

### Prerequisites

* Docker Desktop (Linux containers enabled)
* Git

### Clone the Repository

```bash
git clone https://github.com/JAHNAVISINDHU/multi_tenant_saas.git
cd multi-tenant-saas
```

### Start All Services

```bash
docker-compose down -v
docker-compose up -d
```

---

##  Service URLs

| Service      | URL                                                                  |
| ------------ | -------------------------------------------------------------------- |
| Frontend     | [http://localhost:3000](http://localhost:3000)                       |
| Backend      | [http://localhost:5000](http://localhost:5000)                       |
| Health Check | [http://localhost:5000/api/health](http://localhost:5000/api/health) |

---

##  Authentication Flow

1. Register tenant
2. Login to receive JWT
3. Use token in headers:

```
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI5ODQzMzEzZS00ZjU0LTRiZWEtYjA1Zi1iZTViNmRkNjhjMTQiLCJ0ZW5hbnRJZCI6IjUyYjlhMDQ5LTgyZjctNGE1OS05YjkwLWRkYWM2NjA0YWJhMCIsInJvbGUiOiJ0ZW5hbnRfYWRtaW4iLCJpYXQiOjE3NjYyOTk2NDgsImV4cCI6MTc2NjM4NjA0OH0.AtRK0Y5xCS68eKiEB0GCCFR57-Z5j6NSmcwFAaPr2VM

```

---

##  Subscription Plans

| Plan       | Max Users | Max Projects |
| ---------- | --------- | ------------ |
| Free       | 5         | 3            |
| Pro        | 25        | 15           |
| Enterprise | 100       | 50           |

---

##  Documentation

Detailed documentation is available in the `docs/` folder:

* Research & analysis
* PRD
* Architecture & ERD
* Technical specification

---

##  Notes for Evaluators

* Entire system starts with **one command**
* Database schema & seed data load automatically
* No manual setup required

---

##  Repository Link

[https://github.com/JAHNAVISINDHU/multi_tenant_saas](https://github.com/JAHNAVISINDHU/multi_tenant_saas)
