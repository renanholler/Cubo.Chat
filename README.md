<div align="center">
  <image height="32em" src="https://img.shields.io/badge/nestjs-E0234E?style=for-the-badge&logo=nestjs&logoColor=white" />
  <image height="32em" src="https://img.shields.io/badge/Prisma-3982CE?style=for-the-badge&logo=Prisma&logoColor=white"/>
  <image height="32em" src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=Vite&logoColor=white" />
  <image height="32em" src="https://shields.io/badge/react-black?logo=react&style=for-the-badge" />
  <image height="32em" src="https://img.shields.io/badge/Tailwind_CSS-grey?style=for-the-badge&logo=tailwind-css&logoColor=38B2AC" />
</div>

<img width="1896" alt="capa" src="https://github.com/user-attachments/assets/71c7d4e4-90d4-40d0-af9e-655445ab9acb">

## Installation

After cloning the main repository, you will need to install the dependencies for both the backend and the frontend.

### Clone the Repository

First, clone the repository:

```bash
git clone <repository-url>
cd <repository-name>
```

### Submodules

The subprojects are versioned as submodules in this repository. To download the full content, run the following command:

```bash
git submodule update --init --recursive
```

## Backend Setup

The backend uses **NestJS** and **Prisma** as the ORM to interact with the database. Follow the steps below to set it up:

### 1. Install Dependencies

Navigate to the backend folder and install the dependencies:

```bash
cd backend/
npm install
```

### 2. Configure Environment Variables

Rename the `.env.example` file to `.env`.

### 3. Run Migrations and Seed

To ensure the database is up to date, run the migrations and seed:

```bash
npx prisma migrate dev
```

If the seed does not run automatically, you can execute it manually:

```bash
npx prisma db seed
```

## Frontend Setup

The frontend uses **Vite** for development. Follow the steps below to set it up:

### 1. Install Dependencies

Navigate to the frontend folder and install the dependencies:

```bash
cd frontend/
npm install
```

### 2. Fix Dependency Issues (if necessary)

If you are using a Mac with ARM architecture (Apple Silicon), you may need to follow this procedure to fix optional dependency issues:

1. Delete the `node_modules` folder and the `package-lock.json` file.
2. Clear the npm cache using `npm cache clean --force`.
3. Reinstall the dependencies with `npm install`.

## Running the Projects

### Backend

To run the backend server in development mode:

```bash
cd backend
npm run start:dev
```

### Frontend

To run the frontend server in development mode:

```bash
cd frontend
npm run dev
```
