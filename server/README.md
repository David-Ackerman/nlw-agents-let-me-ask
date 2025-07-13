# Agents Server

This project is a backend server for managing rooms, built as part of the NLW (Next Level Week) event. It provides RESTful endpoints for health checks and room management.

## Technologies Used

- **Node.js**: JavaScript runtime for building scalable server-side applications.
- **TypeScript**: Strongly typed programming language that builds on JavaScript.
- **Drizzle ORM**: TypeScript ORM for SQL databases, used for database schema and migrations.
- **Docker**: Containerization platform for consistent development and deployment environments.
- **HTTPie**: For testing HTTP endpoints (see `client.http`).

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- [Docker](https://www.docker.com/) (for running the database)
- [pnpm](https://pnpm.io/) or [npm](https://www.npmjs.com/) (for dependency management)

### Installation

1. **Clone the repository:**

   ```sh
   git clone <your-repo-url>
   cd server
   ```

2. **Install dependencies:**

   ```sh
   pnpm install
   # or
   npm install
   ```

3. **Start the database with Docker:**

   ```sh
   docker-compose up -d
   ```

4. **Run database migrations:**

   ```sh
   pnpm drizzle-kit migrate
   # or
   npm run drizzle:migrate
   ```

5. **Seed the database (optional):**

   ```sh
   pnpm tsx src/db/seed.ts
   # or
   npm run seed
   ```

6. **Start the server:**

   ```sh
   pnpm dev
   # or
   npm run dev
   ```

The server will start on [http://localhost:3333](http://localhost:3333).

## API Endpoints

- `GET /health` — Health check endpoint
- `GET /rooms` — List all rooms

You can use the `client.http` file to test the endpoints with HTTPie or VS Code REST Client extension.

---
