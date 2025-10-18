# 🎬 Movie Explorer

A full-stack web application built with **NestJS**, **PostgreSQL**, and **ReactJS** that lets users explore movies using the [TMDB API](https://developer.themoviedb.org/), manage their favorite movies, and maintain their own user accounts through secure JWT authentication.

---

## 🚀 Features

- 🔐 **User Authentication**
  - Sign up and log in using JWT-based authentication.
- 🎥 **Movie Discovery**
  - Browse popular movies and search by title via TMDB API.
- ❤️ **Favorites Management**
  - Add and remove favorite movies (stored in PostgreSQL).
- 🧭 **Modern Tech Stack**
  - Backend: NestJS + TypeORM + PostgreSQL
  - Frontend: ReactJS (Vite) + Context API + Axios
- 🌐 **RESTful API**
  - Clean and modular backend structure following NestJS best practices.

---

## ⚙️ Tech Stack

### Backend

- [NestJS](https://nestjs.com/)
- [TypeORM](https://typeorm.io/)
- [PostgreSQL](https://www.postgresql.org/)
- [Axios](https://axios-http.com/)
- [JWT](https://jwt.io/)
- [bcrypt](https://github.com/kelektiv/node.bcrypt.js)

### Frontend

- [ReactJS](https://react.dev/)
- [Vite](https://vitejs.dev/)
- [Axios](https://axios-http.com/)
- [React Router](https://reactrouter.com/)
- [Context API](https://react.dev/learn/passing-data-deeply-with-context)

---

## 🧩 Environment Variables

Create a `.env` file inside `backend/`:

```env
PORT=3000
DATABASE_HOST=localhost
DATABASE_PORT=5432
DATABASE_USER=postgres
DATABASE_PASSWORD=your_password
DATABASE_NAME=movie_db
JWT_SECRET=your_jwt_secret
TMDB_API_KEY=your_tmdb_key
```

---

## 🐘 Setting up PostgreSQL (Optional with Docker)

You can quickly spin up a local PostgreSQL instance using Docker:

```bash
docker-compose up -d
```

Example `docker-compose.yml`:

```yaml
version: "3.8"
services:
  db:
    image: postgres:15
    restart: always
    environment:
      POSTGRES_USER: postgres
      POSTGRES_PASSWORD: your_password
      POSTGRES_DB: movie_db
    ports:
      - "5432:5432"
    volumes:
      - pgdata:/var/lib/postgresql/data
volumes:
  pgdata:
```

---

## 🛠️ Running the Project Locally

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/movie-explorer.git
cd movie-explorer
```

### 2️⃣ Setup and Run Backend

```bash
cd backend
npm install
npm run start:dev
```

**Backend runs on:** 👉 http://localhost:3000

### 3️⃣ Setup and Run Frontend

```bash
cd ../frontend
npm install
npm run dev
```

**Frontend runs on:** 👉 http://localhost:5173

---

## 🔗 API Endpoints Overview

| Method | Endpoint                | Description                  |
| ------ | ----------------------- | ---------------------------- |
| POST   | `/auth/signup`          | Register a new user          |
| POST   | `/auth/login`           | Log in and receive JWT       |
| GET    | `/movies/popular`       | Get popular movies from TMDB |
| GET    | `/movies/search?q=...`  | Search for movies            |
| GET    | `/movies/favorites`     | Get user's favorite movies   |
| POST   | `/movies/favorites`     | Add movie to favorites       |
| DELETE | `/movies/favorites/:id` | Remove movie from favorites  |

> 🧠 **Note:** Protected routes require `Authorization: Bearer <token>` header.

---

## 🎨 Frontend Pages Overview

| Page      | Description                |
| --------- | -------------------------- |
| Login     | Log into your account      |
| Signup    | Register a new user        |
| Movies    | Browse and search movies   |
| Favorites | View saved favorite movies |

---

## 📸 Preview (Optional)

Add screenshots or GIFs of your app UI here once frontend is ready.

---

## 🧠 Learning Objectives

This project helps you understand:

- **NestJS** modular architecture and service layers
- Integration with external APIs (TMDB)
- Database operations with **TypeORM** & **PostgreSQL**
- Full authentication flow using **JWT**
- Connecting **React** frontend to a RESTful backend

This Readme is written by ChatGPT as I don't have time for this things! ( just kidding actually I am lazy 😅 )
