# NLW Agents Project

This project consists of two main applications: a **server** (Fastify + Drizzle ORM + PostgreSQL) and a **web** frontend (React + Vite).

## Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [Docker](https://www.docker.com/) (for running PostgreSQL easily)

## Getting Started

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd agents
```

---

## Server Setup

### Install dependencies

```bash
cd server
npm install
```

### Start PostgreSQL with Docker

```bash
docker compose up -d
```

This will start a PostgreSQL instance as defined in `server/docker-compose.yml`.

### Run database migrations

```bash
npm run db:migrate
```

### (Optional) Seed the database

```bash
npm run db:seed
```

### Start the server (development mode)

```bash
npm run dev
```

The server will start on the port defined in your `.env` file (create one if needed).

---

## Web Setup

### Install dependencies

```bash
cd ../web
npm install
```

### Start the web application

```bash
npm run dev
```

The web app will be available at [http://localhost:5173](http://localhost:5173) by default.

---

## Environment Variables

The server requires a `.env` file in the `server` directory. You can copy `.env.example` and adjust as needed. The following variables are required:

- `PORT`: The port on which the Fastify server will run. Default is `3333`.
- `DATABASE_URL`: The PostgreSQL connection string. Example: `postgresql://docker:docker@localhost:5432/agents` (matches the Docker setup).
- `GEMINI_API_KEY`: Your Google Gemini API key, required for AI features.  
  You can obtain a Gemini API key by signing up at [Google AI Studio](https://aistudio.google.com/app/apikey).

Example `.env`:

```env
PORT=3333
DATABASE_URL="postgresql://docker:docker@localhost:5432/agents"
GEMINI_API_KEY="your-gemini-api-key"

---

## Main Dependencies

### Server

- fastify
- drizzle-orm
- postgres
- zod
- @google/genai

### Web

- react
- vite

---

## Useful Scripts

- `npm run db:migrate` — Run database migrations
- `npm run db:seed` — Seed the database
- `npm run dev` — Start server or web in development mode

---

## License

MIT
```
