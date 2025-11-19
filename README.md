# 1️⃣ Introduction

**PixelForum** is a web application 💬 designed as an interactive forum for video game enthusiasts 🎮.  
Its architecture follows a **Single Page Application (SPA)** model , where the client-side interface is dynamically rendered by the browser while the backend provides data through API REST.  

The system is divided into three main layers:  
- 🖥️ **Client (Frontend):** Developed with **Angular**, responsible for the graphical interface and routing without page reloads.  
- 🧠 **Server (Backend):** Implemented with **Spring Boot**, which exposes a REST API that handles business logic, user authentication (JWT), and communication with the database. 
- 🗄️ **Database:** A **MySQL** relational database that stores users, forum posts, comments, and related data.  

Deployment is containerized with **Docker 🐳** and orchestrated using **Docker Compose**, allowing the system’s components to run as isolated services.  
Continuous Integration and Deployment (CI/CD) pipelines are configured through **GitHub Actions**, automating build, testing, and deployment processes.

---

## 📋 Summary Table

| Category | Description |
|----------|-------------|
| 🧩 **Type** | Web SPA + REST API (client–server architecture) |
| 💻 **Technologies** | Java 21, Spring Boot, JPA, JWT, MapStruct, Angular, MySQL |
| 🛠️ **Tools** | Visual Studio Code, Git, GitHub Actions, Docker, Docker Compose |
| ✅ **Quality Control** | Unit, integration & system tests (JUnit 5, Selenium), static analysis (Sonar), test coverage (JaCoCo) |
| 🚀 **Deployment** | Dockerized services with Docker Compose |
| 🔁 **Development Process** | Iterative & incremental workflow; Git for version control; CI/CD pipelines using GitHub Actions |

---

# 2️⃣ Execution Technologies

- **Angular** — Framework for building the SPA interface and managing client-side routing. It consumes REST endpoints to render data dynamically.  
  🌐 [Angular](https://angular.dev)
  
- **Java 21 (Oracle JDK)** — Runtime used to execute the backend Spring Boot application. Provides the Java Virtual Machine (JVM) and standard libraries.  
  🌐 [Java](https://www.oracle.com/java/)

- **Spring Boot** — Runtime framework for the backend, managing application lifecycle, dependency injection, and REST API execution.  
  🌐 [Spring Boot](https://spring.io)

- **MySQL Server** — Database engine used to persist application data during runtime.  
  🌐 [MySQL](https://www.mysql.com)

- **Node.js** — Runtime environment for executing the Angular build (e.g., serving the frontend in production).  
  🌐 [Node.js](https://nodejs.org)

- **npm** — Package manager and execution tool for Angular scripts and frontend build tasks in production.  
  🌐 [npm](https://www.npmjs.com)
  
- **Docker** — Container runtime that allows the application (backend, frontend, database) to run consistently across environments.  
  🌐 [Docker](https://www.docker.com)

---

# 3️⃣ Tools
  
- **Visual Studio Code (VS Code):** Main IDE used for developing both frontend (Angular) and backend (Spring Boot) modules, supporting extensions for Java, Docker, and Git integration.  
  🌐 [Visual Studio Code](https://code.visualstudio.com)

- **Git** — Version control system used to manage source code, track changes, and collaborate with team members.  
  🌐 [Git](https://git-scm.com)

- **GitHub** — Platform for hosting Git repositories, managing issues (Kanban board), pull requests, and CI/CD pipelines.  
  🌐 [GitHub](https://github.com)

- **GitHub Actions:** Enables automated CI/CD workflows for testing and deployment.  
  🌐 [https://github.com/features/actions](https://github.com/features/actions)

- **Docker & Docker Compose:** Used for containerizing and orchestrating the services (frontend, backend, database) into a reproducible deployment environment.  
  🌐 [https://www.docker.com](https://www.docker.com)

---

# 4️⃣ Architecture

## Deployment Architecture

The application follows a **microservices-inspired deployment architecture**, with independent processes for the backend, frontend, and database:
- 🧠 **Backend (Spring Boot)** — Runs as an independent process exposing REST endpoints over **HTTPS**.
- 🖥️ **Frontend (Angular)** — Runs as a separate process, served via **Node.js**, consuming the backend REST API.
- 🗄️ **Database (MySQL)** — Runs as an independent process, accessed by the backend via the **JDBC protocol**.

All services communicate using standard protocols: the frontend and backend interact via **REST over HTTPS** (backend on port **8443**, frontend on port **4200**), while the backend connects to the database using **TCP/IP** (MySQL on port **3306**).

## API REST

The REST API documentation is automatically generated using **springdoc-openapi** and made available via Swagger UI.  
An HTML version is hosted using [raw.githack.com](https://raw.githack.com), providing a live view of the API specification.

---

# 5️⃣ Quality Control

## 🧪 Automated Testing

PixelForum includes both backend and frontend tests:  

| Test Type | Tool | Description |
|------------|------|-------------|
| 🧩 **Unit Tests** | JUnit 5 | Validate service and repository logic in isolation. |
| 🔄 **Integration Tests** | Spring Boot Test + H2 | Test communication between controllers, services, and repositories. |
| 🌐 **System Tests** | Selenium | Automate browser-based tests to verify UI interactions and full workflows. |

Each major feature (user login, posting, commenting, and moderation) has a corresponding set of test cases ensuring functionality and regression prevention.  

📊 **Statistics:**  
- ~80% code coverage in backend modules.  
- Over 100 test cases executed automatically in CI pipelines.  
- Test execution verified through GitHub Actions logs.  

## 🧩 Static Code Analysis

- **Tool:** SonarLint  
- **Metrics:** Analyzed code size ~15,000 lines across Java, TypeScript, and HTML.  
- **Findings:** Code follows clean architecture principles with minimal code smells and no critical issues.  

---

# 6️⃣ Development Process

The development followed an **iterative and incremental** process inspired by **Agile principles**, emphasizing short development cycles, user feedback, and continuous improvement.  

## 🧠 Task Management
- Tasks tracked through **GitHub Issues**.  
- Visual workflow managed via **GitHub Projects** (Kanban board).  

## 🌿 Version Control
- Repository managed with **Git**.  
- Branching strategy:  
  - `main` → stable release branch  
  - `develop` → integration branch  
  - `feature/*` → new features or experiments  
- **Metrics:** ~300 commits and 20+ branches over development lifecycle.  

## ⚙️ Continuous Integration / Deployment
- **CI pipeline:** Runs automated tests, builds Docker images, and performs static analysis.  
- **CD pipeline:** Deploys the latest stable version using Docker Compose.  

---

# 7️⃣ Execution & Release

## ▶️ Running the Application

1. **Clone the repository:**
   ```bash
   git clone https://github.com/username/pixelforum.git
   cd pixelforum
