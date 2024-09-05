#### **Overview**
This document provides a summary of the critical dependencies required for both the backend and frontend components of the application. It includes the main libraries, frameworks, and tools necessary for development, testing, and production deployment.

---

### **1. Backend Key Dependencies**

- **Node.js**: JavaScript runtime environment.
- **Express**: Web framework for building the API backend.
- **Sequelize**: ORM for PostgreSQL to manage database interactions.
- **pg**: PostgreSQL client for Node.js.
- **bcryptjs**: Library for hashing passwords securely.
- **jsonwebtoken**: Library for creating and verifying JWTs (JSON Web Tokens).
- **dotenv**: Loads environment variables from a `.env` file.
- **aws-sdk**: AWS SDK for interacting with AWS services.

#### **Development Tools**
- **TypeScript**: TypeScript compiler for type-checking JavaScript.
- **Mocha & Chai**: Testing framework and assertion library for unit and integration tests.
- **ESLint**: JavaScript linter for code quality.
- **ts-node-dev**: TypeScript execution environment for Node.js with automatic reloading.

---

### **2. Frontend Key Dependencies**

- **Angular**: Framework for building the frontend application.
  - Core Packages: `@angular/core`, `@angular/common`, `@angular/forms`, `@angular/router`.
- **Ionic Framework**: Hybrid mobile app development framework.
  - Core Packages: `@ionic/angular`, `@ionic-native/core`.
- **RxJS**: Reactive programming library for handling asynchronous events.
- **Zone.js**: Angular library for managing asynchronous operations in the app.

#### **Development Tools**
- **Angular CLI**: Command-line interface tool for Angular development.
- **Karma & Jasmine**: Testing framework and test runner for Angular applications.
- **Protractor**: End-to-end testing framework for Angular apps.
- **TypeScript**: TypeScript compiler for developing Angular components.

---

### **Dependency Management**

- **Node Package Manager (NPM)**: All dependencies for both backend and frontend are managed using `npm` and specified in `package.json`.

---

### **Environment Setup**
- Ensure that the following are installed:
  - **Node.js**: Compatible version for both backend and frontend.
  - **TypeScript**: Required for both backend and frontend development.