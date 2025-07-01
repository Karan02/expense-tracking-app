# expense-tracking-app

# 🧾 Expense Tracker App

A full-stack expense management system built with:

- **Frontend**: React + TypeScript + Chakra UI
- **Backend**: Node.js + Express + TypeScript + Prisma
- **Database**: SQLite / PostgreSQL (via Prisma ORM)

---

## 📁 Project Structure

project-root/
├── Backend/
│ ├── src/
│ ├── prisma/
│ └── package.json
└── Frontend/
├── src/
└── package.json


---

## ⚙️ Prerequisites

- [Node.js](https://nodejs.org/) installed
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [Prisma CLI](https://www.prisma.io/docs/getting-started) (auto-installed)

---

## 🚀 Getting Started

### 🔧 Backend Setup (`/Backend`)

1. Navigate to backend directory:

```
 cd Backend
```
# Install dependencies:
```
 npm install
```
# Setup ENV file
Setup .env file:

Create a .env file in /Backend:
```
 DATABASE_URL="file:./dev.db" # Or use PostgreSQL URL for production
 PORT=5000
```
# Generate Prisma Client
```
 npx prisma generate
```
# Run database migrations:
``` 
 npx prisma migrate dev --name init
```

# Seed the database:
```
 npx ts-node prisma/seed.ts
```
# Start backend server:
```
 npm run dev
```
```
 Server runs at http://localhost:5000
```

# Navigate to frontend directory:
```
 cd Frontend
```
# Install dependencies:
```
 npm install
```
# Start the development server:
```
 npm run dev
```
```
 App runs at http://localhost:5173
```
# Make sure the Vite proxy is set in vite.config.ts:
```
server: {
  proxy: {
    '/api': 'http://localhost:5000'
  }
}
```
## Deployment Platforms - Render.com(Backend-nodejs), Vercel(Frontend-reactjs), Railway(PostGRE)
``` https://expense-tracking-frontend-beta.vercel.app/login ```
