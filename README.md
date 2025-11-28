# TaskFlow - Employee & Task Management System

A full-stack web application I built for managing employees and tasks. The app features a React frontend with a Node.js/Express backend, using SQLite for data storage.

## Live Demo

- **Frontend:** https://fullstackww.netlify.app
- **Backend API:** https://full-stack-p0an.onrender.com
- **Repository:** https://github.com/code-with-harish/Full-Stack

**Login with:** `admin@company.com` / `admin123`

> Note: Backend is on Render's free tier - first request may take ~30 seconds if the server was sleeping.

---

## What I Built

### Frontend (React)
- Dashboard with charts showing employee and task statistics
- Employee management - add, edit, delete, search, filter
- Task management with status updates and priority levels
- Kanban-style task board view
- Individual employee profile pages
- Dark/light theme toggle
- Fully responsive design

### Backend (Node.js + Express)
- RESTful API endpoints for all CRUD operations
- JWT-based authentication
- SQLite database with three tables (users, employees, tasks)
- Input validation and error handling
- Protected routes requiring authentication

### Full Stack Integration
- Frontend connects to backend via Axios
- Auth tokens stored in localStorage
- Real-time toast notifications for user feedback
- Deployed separately - frontend on Netlify, backend on Render

---

## Tech Stack

**Frontend:** React 18, React Router, Chart.js, Axios, React Toastify

**Backend:** Node.js, Express, SQLite (better-sqlite3), JWT, bcryptjs

**Deployment:** Netlify (frontend), Render (backend)

---

## Running Locally

### Prerequisites
- Node.js v16+
- npm

### Setup

```bash
# Clone the repo
git clone https://github.com/code-with-harish/Full-Stack.git
cd Full-Stack

# Install backend dependencies
npm install

# Install frontend dependencies
cd client && npm install && cd ..

# Create environment file
cp .env.example .env
# Edit .env and add: JWT_SECRET=any-random-string

# Start both servers
npm run dev
```

The app will be running at:
- Frontend: http://localhost:3000
- Backend: http://localhost:5000

### Test Accounts
| Email | Password |
|-------|----------|
| admin@company.com | admin123 |
| demo@company.com | demo123 |

---

## API Endpoints

### Auth
- `POST /api/auth/register` - Create account
- `POST /api/auth/login` - Login (returns JWT token)
- `GET /api/auth/me` - Get current user (requires auth)

### Employees
- `GET /api/employees` - List all (supports pagination, search, filters)
- `GET /api/employees/:id` - Get one employee with their tasks
- `POST /api/employees` - Create (requires auth)
- `PUT /api/employees/:id` - Update (requires auth)
- `DELETE /api/employees/:id` - Delete (requires auth)

### Tasks
- `GET /api/tasks` - List all (supports pagination, search, filters)
- `GET /api/tasks/:id` - Get single task
- `POST /api/tasks` - Create (requires auth)
- `PUT /api/tasks/:id` - Update (requires auth)
- `DELETE /api/tasks/:id` - Delete (requires auth)

### Dashboard
- `GET /api/dashboard/stats` - Get summary statistics

---

## Project Structure

```
Full-Stack/
├── client/                 # React app
│   └── src/
│       ├── components/     # Navbar
│       ├── context/        # Auth & Theme state
│       ├── pages/          # Dashboard, Employees, Tasks, etc.
│       └── services/       # API configuration
│
├── server/                 # Express server
│   ├── config/            # Database setup
│   ├── middleware/        # JWT auth
│   └── routes/            # API routes
│
├── package.json
└── README.md
```

---

## Database Schema

Three tables: `users` (for auth), `employees`, and `tasks`.

Tasks have a foreign key to employees (assignee) and users (creator).

The database auto-creates tables and seeds sample data on first run.

---

## Features I Added Beyond Requirements

1. JWT authentication with protected routes
2. Dark mode with preference saved to localStorage
3. Kanban board view for tasks
4. Employee profile pages with task statistics
5. Charts on dashboard using Chart.js
6. Overdue task highlighting
7. Quick inline status updates
8. Toast notifications
9. Responsive design for mobile
10. Deployed to cloud (Netlify + Render)

---

## Assumptions

- Single organization use (no multi-tenancy)
- SQLite chosen for simplicity - easily swappable to PostgreSQL
- Avatars show initials instead of uploaded images
- Demo data is seeded automatically

---

## Author

Built by Harish as a full-stack development assignment by .

---

**Live at:** https://fullstackww.netlify.app
