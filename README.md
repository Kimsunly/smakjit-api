# SmakJit API

Production-ready REST API for the **SmakJit Volunteer Management Platform** built with **Laravel**.

This backend provides authentication, role-based access control, volunteer workflows, event management, and integration-ready endpoints for modern frontend clients such as **Next.js**.

Designed following scalable REST architecture principles and service-layer separation to support future expansion into a full production deployment environment.

---

# 📌 Project Overview

SmakJit is a volunteer management platform that helps organizations:

* Manage volunteers efficiently
* Create and control events
* Track participation
* Handle application workflows
* Provide role-based system access

This repository contains the backend API powering the platform.

---

# 🧰 Tech Stack

### Backend Framework

* Laravel 13

### Database

* MySQL

### Authentication

* Laravel Sanctum (Token-based authentication)

### Architecture

* REST API
* Service Layer Pattern
* Form Request Validation
* API Resource Transformation

### Integration Target

* Next.js Frontend Client

---

# 🚀 Core Features

## Authentication System

* Register user
* Login user
* Logout user
* Token-based authentication
* Protected API routes

## User Management

* User profile management
* Role assignment
* Role-based authorization

## Volunteer Module

* Volunteer registration
* Volunteer profile update
* Participation tracking

## Event Management

* Create events
* Update events
* Delete events
* Browse events

## Application Workflow

* Apply to events
* Approve applications
* Reject applications
* Track application status

## System Utilities

* API health check endpoint
* Validation layer
* Error handling structure
* Clean response formatting

---

# 🏗️ System Architecture

The project follows a layered architecture:

### Controllers

Handle incoming requests and responses

### Services

Contain business logic

### Requests

Validate incoming request data

### Resources

Format API responses

### Models

Interact with database tables

Example structure:

```
app/
 ├── Http/
 │   ├── Controllers/API
 │   ├── Requests
 │   └── Resources
 ├── Models
 └── Services
```

---

# ⚙️ Installation Guide

Clone repository:

```
git clone https://github.com/YOUR_USERNAME/smakjit-api.git
```

Move into project directory:

```
cd smakjit-api
```

Install dependencies:

```
composer install
```

Copy environment file:

```
cp .env.example .env
```

Generate application key:

```
php artisan key:generate
```

Configure database inside `.env`

Example:

```
DB_DATABASE=smakjit
DB_USERNAME=root
DB_PASSWORD=
```

Run migrations:

```
php artisan migrate
```

Run development server:

```
php artisan serve
```

Server runs at:

```
http://localhost:8000
```

---

# 🌐 API Base URL

```
http://localhost:8000/api
```

Health check endpoint:

```
GET /api/health
```

Example response:

```
{
  "status": "ok",
  "service": "SmakJit API"
}
```

---

# 🔐 Authentication Strategy

This API uses **Laravel Sanctum token-based authentication**

Workflow:

### Register

User registers account

### Login

Server returns access token

### Access Protected Routes

Frontend sends token in header:

```
Authorization: Bearer YOUR_ACCESS_TOKEN
```

### Logout

Token revoked from server

---

# 🌳 Branch Strategy

The repository follows structured Git workflow

### Main branch

Production-ready code

### Develop branch

Integration branch

### Feature branches

Used for module development

Example naming:

```
feature/authentication
feature/events-module
feature/volunteer-module
```

Workflow example:

```
feature → develop → main
```

---

# 📁 Folder Structure

Project follows scalable backend folder structure

```
app/

Http/

Controllers/API/

Requests/

Resources/

Models/

Services/
```

Future extension folders:

```
Repositories/
Traits/
Enums/
Policies/
```

---

# 📐 API Development Standards

Controller responsibilities:

* Receive request
* Call service layer
* Return API resource response

Business logic belongs inside:

```
app/Services
```

Validation belongs inside:

```
app/Http/Requests
```

Response formatting belongs inside:

```
app/Http/Resources
```

---

# 📬 Example API Response Format

Success response example:

```
{
  "status": "success",
  "data": {}
}
```

Error response example:

```
{
  "status": "error",
  "message": "Unauthorized"
}
```

---

# 🔧 Environment Variables

Example configuration inside `.env`

```
APP_NAME=SmakJit
APP_ENV=local
APP_DEBUG=true
APP_URL=http://localhost:8000

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=smakjit
DB_USERNAME=root
DB_PASSWORD=
```

---

# 🧪 Testing Strategy (Planned)

* Unit testing
* Feature testing
* Authentication testing
* API endpoint testing

Example command:

```
php artisan test
```

---

# 🚀 Deployment Strategy (Future Ready)

This backend is structured for deployment to:

* VPS servers
* Docker containers
* Cloud platforms

Example platforms:

* AWS
* DigitalOcean
* Render

---

# 🔒 Security Strategy

* Sanctum authentication
* Role-based authorization
* Input validation layer
* Hidden sensitive environment variables
* Token protection middleware

---

# 🔗 Integration Target

Primary frontend integration target:

Next.js SmakJit frontend

Communication via REST API:

```
JSON responses
Bearer tokens
Protected routes
```

---

# 👨‍💻 Team

**KimsunLy** **LyMengHong** **RethChanRith** **PechSuyHeng** **MeachKimHab** **ThoeurnKimChhay**

Information Technology and Engineering Student
Royal University of Phnom Penh

Backend Developer Track focused on building scalable backend systems using Laravel REST architecture.
