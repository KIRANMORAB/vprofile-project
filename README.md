# vProfile Project

A **Dockerized, three-tier web application** for profile management—combining **MySQL** (database), **Tomcat** (application server), and **Nginx** (web server) using **Docker Compose**.

---
A **Dockerized, three-tier web application** for profile management—combining **MySQL** (database), **Tomcat** (application server), and **Nginx** (web server) using **Docker Compose**.

## 🎥 Demo Video

Watch the vProfile Project Docker Compose demo here:  
[![vProfile Demo Video](https://img.youtube.com/vi/vP8O6NOU0h4/0.jpg)](https://youtu.be/vP8O6NOU0h4?si=d-LQSNr2RNY-NsPE)


## 🚀 Features

- 🗝 **User Authentication**: Secure login and user sessions.  
- 📂 **Profile CRUD Operations**: Create, read, update, and delete user profiles.  
- 🔗 **RESTful API**: Accessible to front-end applications and third-party integrations.  
- 🏗 **3-Tier Architecture**: Clear separation of web, application, and database layers—all containerized.

---

## 🖥 Architecture Overview

```
┌──────────────┐       ┌──────────────┐       ┌──────────────┐
│   vproweb    │  →    │   vproapp    │  →    │   vprodb     │
│  (Nginx)     │       │ (Tomcat App) │       │   (MySQL)    │
└──────────────┘       └──────────────┘       └──────────────┘
```

- **vproweb**: Serves as the front-facing web layer via Nginx.  
- **vproapp**: Handles application logic using Tomcat.  
- **vprodb**: Stores persistent data in MySQL.

---

## ✅ Prerequisites

- Docker installed  
- Docker Compose installed  

---

## ⚡ Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/kiranmorab/vprofile-project.git
   cd vprofile-project
   ```

2. **Build and start all services**
   ```bash
   docker-compose up -d --build
   ```

3. **Access the application**
   - 🌍 Web interface: [http://localhost](http://localhost)  
   - ⚙️ API / Tomcat (if exposed): [http://localhost:8080](http://localhost:8080)  
   - 🗄 MySQL Port: `localhost:3306`

---

## 📂 Development Folder Structure

```
.
├── Docker-files/
│   ├── db/       # MySQL Dockerfile & configs
│   ├── app/      # Tomcat (Java) Dockerfile & configs
│   └── web/      # Nginx Dockerfile & configs
├── src/          # Source code for the application (Java, JSP, etc.)
├── docker-compose.yml
├── pom.xml       # Maven build configuration
└── README.md
```

---

## 🎯 Why This Project?

- **Great for Learning**: Ideal for DevOps practitioners to understand containerized multi-tier architecture.  
- **Easy Setup**: Launches a full-stack application with a single command via Docker Compose.  
- **Modular & Scalable**: Each service runs in its own container, making it easy to extend or replace components.

---

## 🔮 Optional Enhancements

- Add GitHub badges (e.g., Docker, Java, MySQL, Nginx, Build Status).  
- Include a UML or flowchart to visualize system interactions.  
- Provide API documentation (Swagger or README-styled reference).

---
