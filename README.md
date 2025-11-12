# 1️⃣ Introduction

**PixelForum** is a web application 💬 designed as an interactive forum for video game enthusiasts 🎮.  
Its architecture follows a **Single Page Application (SPA)** model ⚙️, where the client-side interface is dynamically rendered by the browser while the backend provides data through a RESTful API.  

The system is divided into three main layers:  
- 🖥️ **Client (Frontend):** Developed with **Angular**, responsible for the graphical interface and routing without page reloads.  
- 🧠 **Server (Backend):** Implemented with **Spring Boot**, which exposes a REST API that handles business logic, user authentication (via JWT 🔐), and communication with the database.  
- 🗄️ **Database:** A **MySQL** relational database that stores users, forum posts, comments, and related data.  

Deployment is containerized with **Docker 🐳** and orchestrated using **Docker Compose**, allowing the system’s components to run as isolated services.  
Continuous Integration and Deployment (CI/CD ⚡) pipelines are configured through **GitHub Actions**, automating build, testing, and deployment processes.

---

## 📋 Summary Table

| Category | Description |
|-----------|-------------|
| 🧩 **Type** | Web SPA + REST API |
| 💻 **Technologies** | Java 21, Spring Boot, JPA, JWT, MapStruct, Angular, MySQL |
| 🛠️ **Tools** | Visual Studio Code, Git, GitHub Actions, Docker, Docker Compose |
| ✅ **Quality Control** | Unit & integration tests (JUnit 5, Selenium), static analysis (SonarLint) |
| 🚀 **Deployment** | Dockerized services orchestrated with Docker Compose |
| 🔁 **Development Process** | Iterative & incremental, Agile-inspired (XP, Kanban), GitHub Projects, CI/CD pipelines |

---

# 2️⃣ Technologies

- ⚡ **Angular** — Framework for building the SPA interface and managing client-side routing. It consumes REST endpoints to render data dynamically.  
  🌐 [https://angular.io](https://angular.io)

- ☕ **Spring Boot** — Backend framework used to build the REST API and manage dependencies, configuration, and application lifecycle.  
  🌐 [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot)

- 🧱 **JPA (Java Persistence API)** — Abstraction layer for database communication, simplifying CRUD operations with MySQL through ORM mapping.  
  🌐 [https://jakarta.ee/specifications/persistence](https://jakarta.ee/specifications/persistence)

- 🔐 **JWT (JSON Web Token)** — Used for stateless authentication between the client and server.  
  🌐 [https://jwt.io](https://jwt.io)

- 🔄 **MapStruct** — Code generator for automatic mapping between entities and DTOs.  
  🌐 [https://mapstruct.org](https://mapstruct.org)

- 🗃️ **MySQL** — Relational database system used to persist forum data, users, and interactions.  
  🌐 [https://www.mysql.com](https://www.mysql.com)

---

# 3️⃣ Tools

- 💻 **Visual Studio Code (VS Code):** Main IDE used for developing both frontend (Angular) and backend (Spring Boot) modules, supporting extensions for Java, Docker, and Git integration.  
  🌐 [https://code.visualstudio.com](https://code.visualstudio.com)

- 🧰 **Git & GitHub:** Used for version control, task tracking (Issues), and project management (Projects and Kanban boards).  
  🌐 [https://github.com](https://github.com)

- 🐳 **Docker & Docker Compose:** Used for containerizing and orchestrating the services (frontend, backend, database) into a reproducible deployment environment.  
  🌐 [https://www.docker.com](https://www.docker.com)

- ⚙️ **GitHub Actions:** Enables automated CI/CD workflows for testing and deployment.  
  🌐 [https://github.com/features/actions](https://github.com/features/actions)

- 🧹 **SonarLint:** Static code analysis tool integrated into the IDE to detect code smells, bugs, and maintain quality standards.  
  🌐 [https://www.sonarlint.org](https://www.sonarlint.org)

---

# 4️⃣ Architecture

## 🏗️ Deployment Architecture

PixelForum is deployed using a **three-service Docker Compose setup**:  
- 🧠 **Backend container** running Spring Boot.  
- 🖥️ **Frontend container** built from the Angular project and served via Nginx.  
- 🗄️ **Database container** running MySQL.  

All services communicate using REST over HTTP (port 8080 for backend, 4200 for frontend).  
The architecture ensures scalability, modularity, and ease of deployment across environments.

## 🔗 API REST Documentation

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
