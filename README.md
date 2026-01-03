# Multi-Tenant SaaS Platform
Production-ready multi-tenant project & task management SaaS application.

---

## Features
- Multi-tenant data isolation (per-tenant separation)
- JWT-based authentication
- Role-based access control:
  - super_admin
  - tenant_admin
  - user
- Secure project and task management
- Automatic database migrations and seed data on startup
- Fully dockerized setup (database, backend, frontend)
- Health check endpoint available

---

### Tech Stack
- Backend
- Node.js
- Express.js
- PostgreSQL
- JWT Authentication
- Role-Based Access Control (RBAC)

---

## Frontend
- React (Vite)
- Axios
- Role-based UI rendering

## Infrastructure
- Docker
- Docker Compose

### Quick Start

# From repository root
docker-compose up -d

# Verify backend health
curl http://localhost:5000/api/health

# Open frontend
http://localhost:3000/

No manual database setup is required.
Migrations and seed data run automatically.

---

Access URLs
Service:
Frontend	http://localhost:3000
Backend API	http://localhost:5000
Health Check	http://localhost:5000/api/health

---

### Seeded Credentials (For Evaluation)
Tenant Admin
Email: admin@acet.com
Password: Admin@123
Tenant Subdomain: acet
These credentials are also listed in submission.json.

---

### How to Login
- Open: http://localhost:3000/login
- Enter the credentials above
- Click Login
- You will be redirected to the dashboard
  
This account allows access to:
- User management
- Project creation
- Task management
- Tenant-level administration
  
### Authentication & Roles
- super_admin – System-wide administrator
- tenant_admin – Manages users and resources within a tenant
- user – Regular tenant user
Each tenant’s data is fully isolated from other tenants.

### Docker Services (Fixed Names & Ports)
- database — PostgreSQL (5432 → 5432)
- backend — Node.js / Express API (5000 → 5000)
- frontend — React app (3000 → 3000)

### Project Structure
- Backend: backend/src
- Database migrations: backend/migrations
- Seed data: backend/seed.js
- Frontend: frontend/src
- Docker Compose: docker-compose.yml

### Testing the Application
1. After startup:
2. Open the frontend
3. Login using seeded credentials
Verify:
 - Tenant isolation
 - Role-based access
 - Project & task operations

### Demo Video
A complete demo covering:

- Architecture overview
- Docker startup
- Multi-tenancy flow
- User, project, and task management

### Demo link:
https://drive.google.com/file/d/19-I6o1B8UJIXyF1PfAJmPYbNrVQXAOih/view

### Notes for Evaluators
- Fully dockerized application
- Single-command startup: docker-compose up -d
- Automatic migrations and seed data
- No manual setup required

---

### Summary:
This project is a fully dockerized multi-tenant SaaS application that demonstrates secure tenant isolation and role-based access control.
It enables multiple organizations to manage users, projects, and tasks within a shared system while keeping data strictly separated.
The backend API, frontend application, and database run as independent services using Docker and Docker Compose.
The architecture follows real-world SaaS design patterns including authentication, authorization, and database migrations.
This project is built for scalability, practical learning, and academic evaluation.
