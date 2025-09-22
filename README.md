# Pruebas
## Summary
🎮 This video game forum web application is designed for players 👾 who want to share their experiences, discuss their favorite titles, and connect with other gamers around the world 🌍.
Instead of a large generic forum where all kinds of unrelated topics are mixed ❌, this platform is focused exclusively on video games 🕹️, creating a dedicated space for players.
The application lets users create posts ✍️, comment on discussions 💬, give likes 👍, and customize their profile with an avatar 👤. In addition, it offers structured categories by game 🎯, image uploads 📷, popularity charts 📊, notifications 🔔, and advanced features such as user reputation, trending posts, and real-time updates ⚡, providing a complete and organized platform for gamer interaction 🚀.

At this stage, only the functional and technical objectives of the application have been defined. The development and implementation of the system have not yet started.

## 🎯 Objectives
### ✅ Functional Objectives
The main functional objective of this application is to provide an online forum specialized in video games, where users can interact in an easy and dynamic way. The platform aims to facilitate the creation and participation in discussions, organize topics by game categories, and strengthen the community through social interaction tools and multimedia content.

Planned functionalities:
1. User registration and authentication with customizable profiles (including avatar).
2. Creation of posts related to video games.
3. Comment system on posts to encourage participation.
4. Possibility to give likes to posts and comments.
5. Organization of content through categories and specific games.
6. Image upload for profiles and posts.
7. Visualization of charts about game popularity or user activity.
8. Real-time email notifications.

### ⚙️ Technical Objectives
From a technical perspective, the application is conceived as a modern web development based on robust and scalable technologies. The goal is to implement a secure backend with API support, a dynamic frontend that ensures a good user experience, and complementary features such as chart visualization, file upload, and integration of external services.

Planned technical aspects:
1. Development with Spring Boot (Java) for business logic and REST APIs.
2. Development of the frontend with Angular to create a dynamic, modular, and maintainable user interface, ensuring a smooth interaction with the backend through REST APIs.
3. Relational database (MySQL) for managing users, posts, comments, and games.
4. Image upload implementation.
5. Implementation of automated testing using JUnit for backend unit and integration tests, and Selenium for frontend end-to-end testing of the web interface.
6. Integration of notifications via email and/or websockets.
7. Security through authentication and authorization with JWT.
8. Static code analysis with cloud-based tools (SonarQube) to continuously monitor code quality and review reported issues throughout the development process.
9. Native packaging with GraalVM to generate a native image of the backend application, improving performance and reducing startup time.

## 🛠️ Methodology
The development of this project will follow a high-level iterative methodology, dividing the work into several clearly defined phases. Each phase has specific goals and deliverables, and the progress will be continuously monitored to ensure the quality and consistency of the implementation. This approach allows for incremental improvements, early detection of issues, and adaptation to feedback throughout the project.

### 📅 Phases
- Phase 1 – Definition of functionalities:
In this phase, the general and detailed functionalities of the application will be defined. Additionally, initial wireframes and navigation flow designs will be created to guide the structure and user experience.

- Phase 2 – Configuration of technologies and development tools:
Setup of the development environment, integration of frameworks and libraries, and periodic quality controls (code analysis, testing tools) will be performed.

- Phases 3, 4, 5 – Iterative and incremental development:
The application will be developed in small increments. Each iteration will implement features from the simplest to the more complex, allowing for continuous testing, feedback, and improvement. At the end of each phase, a version (release) of the application will be published for review and testing.

- Phase 6 – Writing the final report:
The memory/documentation of the project will be drafted, including objectives, design, implementation details, and conclusions.

- Phase 7 – Preparation of the presentation:
The final presentation for the defense will be prepared, including slides, demos, and supporting materials.

### ⏳ Timeline
|  Phase  | Start | End |
|---------|-------|-----|
| Phase 1 | 17/09/2025 |  |
| Phase 2 |  |  |
| Phase 3 |  |  |
| Phase 4 |  |  |
| Phase 5 |  |  |
| Phase 6 |  |  |
| Phase 7 |  |  |

### 📊 Gantt Chart
A Gantt chart will be created to visually represent these phases, showing the schedule, dependencies, and milestones.

## 📋 Detailed Functionalities
The functionalities of the application are classified according to their complexity and the type of user they target. They are divided into basic, intermediate, and advanced functionalities to clearly define their scope and purpose. *‘Only owned’ means the user can only modify or delete their own information.

### Basic Functionalities
|  Functionality  | Guest User | Registered User | Administartor |
|---------|-------|-----|-----|
| Registration/Login | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| View Post | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| View public profile | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| Create/Edit/Delete Post | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) (Only owned) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| Create/Edit/Delete Comment | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) (Only owned) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| Give likes | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| Add topic to post | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| Upload image to profile and post | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |

### Intermediate Functionalities
|  Functionality  | Guest User | Registered User | Administartor |
|---------|-------|-----|-----|
| View private profile data | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) (Only owned) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| Create/Edit/Remove topics | ![No](https://img.shields.io/badge/No-red) | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| View charts | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| View trending posts | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| Admin posts and comments | ![No](https://img.shields.io/badge/No-red) | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |

### Advanced Functionalities
|  Functionality  | Guest User | Registered User | Administartor |
|---------|-------|-----|-----|
| Recieve notifications | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) (Only owned) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| Recommendation algorithm | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| Password recovery | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |
| Ban users | ![No](https://img.shields.io/badge/No-red) | ![No](https://img.shields.io/badge/No-red) | ![Yes](https://img.shields.io/badge/Yes-brightgreen) |



## 📌 Tracking / Progress
Project blog: A blog will be maintained with announcements and updates about the development of the project.
GitHub Project: A GitHub Project board will be used to manage tasks, track progress, and organize development activities.

## 👤 Author
Introduction: This application is developed in the context of the Bachelor’s Degree Final Project for the Computer Science degree at the ETSII of URJC.
Author and Supervisor:
| Role | Name | Mail | GitHub |
|---------|-----------|----------------------------|---------|
| Student | Martín Gutiérrez Parada | m.gutierrezp.2022@alumnos.urjc.com | [GitHub](https://github.com/martingutpar) |
| Tutor | Michel Maes Bermejo | michel.maes@urjc.es | [GitHub](https://github.com/Maes95) |
