# 🚀 TaskFlow - Employee & Task Management System

A comprehensive full-stack web application for managing employees and tasks, built with modern technologies.

---

## 🌐 Live Demo

| Service | URL |
|---------|-----|
| **🖥️ Frontend (Netlify)** | [https://fullstackww.netlify.app](https://fullstackww.netlify.app) |
| **⚙️ Backend API (Render)** | [https://full-stack-p0an.onrender.com](https://full-stack-p0an.onrender.com) |
| **📂 GitHub Repository** | [https://github.com/code-with-harish/Full-Stack](https://github.com/code-with-harish/Full-Stack) |

### 🔑 Demo Credentials
```
Email: admin@company.com
Password: admin123
```

> **Note:** The backend is hosted on Render's free tier, which may take 30-60 seconds to wake up on first request after inactivity.

---

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Screenshots](#-screenshots)
- [Setup Instructions](#-setup-instructions)
- [API Documentation](#-api-documentation)
- [Project Structure](#-project-structure)
- [Bonus Features](#-bonus-features)
- [Assumptions](#-assumptions)

---

## ✨ Features

### 🎨 Frontend (Track 1)
| Feature | Description |
|---------|-------------|
| 📱 Responsive Design | Works seamlessly on desktop, tablet, and mobile |
| 🎨 Modern UI | Clean interface with smooth animations and transitions |
| 📊 Interactive Dashboard | Chart.js visualizations for data insights |
| 🔍 Search & Filter | Advanced filtering for employees and tasks |
| 📄 Pagination | Efficient data handling for large datasets |
| ✅ Form Validation | Client-side validation with user feedback |
| 🌓 Dark Mode | Toggle between light and dark themes |
| 📋 Kanban Board | Visual task management with columns |
| 👤 Employee Profiles | Detailed employee pages with task history |

### ⚙️ Backend (Track 2)
| Feature | Description |
|---------|-------------|
| 🔐 JWT Authentication | Secure token-based authentication system |
| 🛡️ Protected Routes | Middleware-based route protection |
| 📝 CRUD Operations | Full Create, Read, Update, Delete for all entities |
| ✅ Input Validation | Server-side validation using express-validator |
| 🗄️ SQLite Database | Lightweight database with proper schema design |
| 📈 Statistics API | Dashboard analytics and reporting |
| 🏥 Health Check | Deployment monitoring endpoint |

### 🔗 Full Stack Integration (Track 3)
| Feature | Description |
|---------|-------------|
| 🔄 Real-time Sync | Seamless data synchronization |
| 👤 Auth Flow | Complete login/register user flow |
| 🍞 Toast Notifications | Real-time user feedback |
| 🎯 Error Handling | Consistent error handling across stack |
| ☁️ Cloud Deployment | Deployed on Render & Netlify |

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| React 18 | UI Library |
| React Router v6 | Client-side routing |
| Chart.js | Data visualization |
| Axios | HTTP client |
| React Toastify | Notifications |
| React Icons | Icon library |
| CSS3 (Custom) | Styling with CSS Variables, Flexbox, Grid |

### Backend
| Technology | Purpose |
|------------|---------|
| Node.js | Runtime environment |
| Express.js | Web framework |
| SQLite (better-sqlite3) | Database |
| JWT (jsonwebtoken) | Authentication |
| bcryptjs | Password hashing |
| express-validator | Input validation |
| CORS | Cross-origin requests |

### Deployment
| Service | Purpose |
|---------|---------|
| Netlify | Frontend hosting |
| Render | Backend hosting |
| GitHub | Version control |

---

## 📸 Screenshots

### 🔐 Login Page
Modern authentication interface with dark mode support.
- Clean, centered design
- Demo credentials displayed
- Form validation feedback

### 📊 Dashboard
Interactive analytics dashboard featuring:
- **Summary Cards** - Total employees, tasks, completion rate
- **Doughnut Chart** - Task status distribution
- **Bar Chart** - Employees by department
- **Recent Activity** - Latest employees and upcoming deadlines

### 👥 Employees Page
Comprehensive employee management:
- **Search** - Filter by name, email, position
- **Filters** - Department and status dropdowns
- **CRUD** - Add, Edit, Delete employees
- **Pagination** - Navigate through records
- **Status Badges** - Visual status indicators

### 👤 Employee Profile
Detailed individual employee view:
- **Info Card** - Contact details, department, position
- **Task Stats** - Completed, in-progress, pending counts
- **Task Distribution Chart** - Visual breakdown
- **Assigned Tasks List** - All tasks for this employee

### ✅ Tasks Page
Task list management with:
- **Quick Status Update** - Change status inline
- **Priority Indicators** - Color-coded badges
- **Overdue Highlighting** - Red badges for overdue tasks
- **Assignee Display** - Show assigned employee

### 📋 Task Board (Kanban)
Visual project management:
- **Three Columns** - Pending, In Progress, Completed
- **Task Cards** - Priority, due date, assignee
- **Add Tasks** - Create directly on board
- **Edit/Delete** - Manage tasks from cards

### 🌓 Dark Mode
Full theme support:
- **Toggle Button** - In navigation bar
- **Persisted** - Saves preference to localStorage
- **Complete Coverage** - All components styled

---

## 🚀 Setup Instructions

### Prerequisites
- **Node.js** v16 or higher
- **npm** or **yarn**
- **Git**

### Step 1: Clone Repository
```bash
git clone https://github.com/code-with-harish/Full-Stack.git
cd Full-Stack
```

### Step 2: Install Dependencies
```bash
# Install server dependencies
npm install

# Install client dependencies
cd client && npm install && cd ..
```

### Step 3: Environment Setup
```bash
# Create .env file in root directory
cp .env.example .env

# Edit .env with your values:
# PORT=5000
# JWT_SECRET=your-super-secret-key-here
# NODE_ENV=development
```

### Step 4: Start Development Servers

**Option A: Run both servers concurrently**
```bash
npm run dev
```

**Option B: Run separately**
```bash
# Terminal 1 - Backend (port 5000)
npm run server

# Terminal 2 - Frontend (port 3000)
npm run client
```

### Step 5: Access Application
- **Frontend:** http://localhost:3000
- **Backend API:** http://localhost:5000/api
- **API Health:** http://localhost:5000/api/health

### Demo Accounts
| Role | Email | Password |
|------|-------|----------|
| Admin | admin@company.com | admin123 |
| Demo | demo@company.com | demo123 |

---

## 📚 API Documentation

### Base URL
- **Local:** `http://localhost:5000/api`
- **Production:** `https://full-stack-p0an.onrender.com/api`

### Authentication Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| POST | `/auth/register` | Register new user | ❌ |
| POST | `/auth/login` | Login user | ❌ |
| GET | `/auth/me` | Get current user | ✅ |

**Login Request:**
```json
POST /api/auth/login
{
  "email": "admin@company.com",
  "password": "admin123"
}
```

**Login Response:**
```json
{
  "message": "Login successful",
  "token": "eyJhbGciOiJIUzI1NiIs...",
  "user": {
    "id": 1,
    "username": "admin",
    "email": "admin@company.com",
    "role": "admin"
  }
}
```

### Employee Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| GET | `/employees` | Get all employees (paginated) | ❌ |
| GET | `/employees/:id` | Get single employee with tasks | ❌ |
| POST | `/employees` | Create employee | ✅ |
| PUT | `/employees/:id` | Update employee | ✅ |
| DELETE | `/employees/:id` | Delete employee | ✅ |
| GET | `/employees/departments` | Get department list | ❌ |

**Query Parameters:**
- `page` - Page number (default: 1)
- `limit` - Items per page (default: 10)
- `search` - Search by name, email, position
- `department` - Filter by department
- `status` - Filter by active/inactive

### Task Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| GET | `/tasks` | Get all tasks (paginated) | ❌ |
| GET | `/tasks/:id` | Get single task | ❌ |
| POST | `/tasks` | Create task | ✅ |
| PUT | `/tasks/:id` | Update task | ✅ |
| DELETE | `/tasks/:id` | Delete task | ✅ |

**Query Parameters:**
- `page` - Page number (default: 1)
- `limit` - Items per page (default: 10)
- `search` - Search by title, description
- `status` - pending/in_progress/completed
- `priority` - low/medium/high
- `employee_id` - Filter by assignee

### Dashboard Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| GET | `/dashboard/stats` | Get statistics | ❌ |
| GET | `/dashboard/performance` | Get employee performance | ❌ |

---

## 📁 Project Structure

```
Full-Stack/
├── 📂 client/                      # React Frontend
│   ├── 📂 public/
│   │   ├── index.html
│   │   └── manifest.json
│   └── 📂 src/
│       ├── 📂 components/
│       │   └── Navbar.js           # Navigation with theme toggle
│       ├── 📂 context/
│       │   ├── AuthContext.js      # Authentication state
│       │   └── ThemeContext.js     # Dark mode state
│       ├── 📂 pages/
│       │   ├── Dashboard.js        # Analytics dashboard
│       │   ├── Employees.js        # Employee CRUD
│       │   ├── EmployeeProfile.js  # Employee details
│       │   ├── Login.js            # Authentication
│       │   ├── Tasks.js            # Task list
│       │   └── TaskBoard.js        # Kanban board
│       ├── 📂 services/
│       │   └── api.js              # Axios configuration
│       ├── App.js                  # Routes & layout
│       ├── index.css               # Global styles
│       └── index.js                # Entry point
│
├── 📂 server/                      # Node.js Backend
│   ├── 📂 config/
│   │   └── database.js             # SQLite setup & seeding
│   ├── 📂 data/
│   │   └── database.sqlite         # SQLite database
│   ├── 📂 middleware/
│   │   └── auth.js                 # JWT middleware
│   ├── 📂 routes/
│   │   ├── auth.js                 # Auth routes
│   │   ├── dashboard.js            # Stats routes
│   │   ├── employees.js            # Employee routes
│   │   └── tasks.js                # Task routes
│   └── index.js                    # Express entry
│
├── .env.example                    # Environment template
├── .gitignore                      # Git ignore rules
├── netlify.toml                    # Netlify config
├── render.yaml                     # Render config
├── package.json                    # Dependencies
└── README.md                       # Documentation
```

---

## 🌟 Bonus Features Implemented

| # | Feature | Description |
|---|---------|-------------|
| 1 | 🔐 JWT Authentication | Secure token-based auth with protected routes |
| 2 | 📊 Interactive Charts | Chart.js visualizations on dashboard |
| 3 | 📱 Responsive Design | Mobile-first approach, works on all devices |
| 4 | 🍞 Toast Notifications | Real-time feedback using react-toastify |
| 5 | 🔍 Advanced Filtering | Multiple filters with search and pagination |
| 6 | 🌱 Database Seeding | Auto-populated demo data on startup |
| 7 | ✅ Input Validation | Client + server-side validation |
| 8 | 🎯 Error Handling | Comprehensive error messages |
| 9 | ⚡ Quick Status Toggle | Update task status inline |
| 10 | ⏰ Overdue Detection | Visual indicators for overdue tasks |
| 11 | 🌓 Dark Mode | Theme toggle with localStorage persistence |
| 12 | 📋 Kanban Board | Visual task management view |
| 13 | 👤 Employee Profiles | Detailed pages with task stats |
| 14 | ☁️ Cloud Deployment | Live on Render + Netlify |

---

## 📝 Assumptions

1. **Single Organization** - App designed for single company use
2. **SQLite Database** - Chosen for simplicity; easily swappable to PostgreSQL/MySQL
3. **No File Uploads** - Avatars use initials instead of images
4. **Modern Browsers** - Targets Chrome, Firefox, Safari, Edge
5. **Demo Data** - Database auto-seeds with sample data on first run

---

## 🗄️ Database Schema

```sql
-- Users (Authentication)
CREATE TABLE users (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  username TEXT UNIQUE NOT NULL,
  email TEXT UNIQUE NOT NULL,
  password TEXT NOT NULL,
  role TEXT DEFAULT 'user',
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  updated_at DATETIME DEFAULT CURRENT_TIMESTAMP
);

-- Employees
CREATE TABLE employees (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  first_name TEXT NOT NULL,
  last_name TEXT NOT NULL,
  email TEXT UNIQUE NOT NULL,
  phone TEXT,
  department TEXT NOT NULL,
  position TEXT NOT NULL,
  salary REAL,
  hire_date DATE NOT NULL,
  status TEXT DEFAULT 'active',
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  updated_at DATETIME DEFAULT CURRENT_TIMESTAMP
);

-- Tasks
CREATE TABLE tasks (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  title TEXT NOT NULL,
  description TEXT,
  status TEXT DEFAULT 'pending',
  priority TEXT DEFAULT 'medium',
  due_date DATE,
  employee_id INTEGER REFERENCES employees(id),
  created_by INTEGER REFERENCES users(id),
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  updated_at DATETIME DEFAULT CURRENT_TIMESTAMP
);
```

---

## 🧪 Testing the API

### Using cURL

```bash
# Health Check
curl https://full-stack-p0an.onrender.com/api/health

# Login
curl -X POST https://full-stack-p0an.onrender.com/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{"email":"admin@company.com","password":"admin123"}'

# Get Employees
curl https://full-stack-p0an.onrender.com/api/employees

# Get Tasks
curl https://full-stack-p0an.onrender.com/api/tasks

# Get Dashboard Stats
curl https://full-stack-p0an.onrender.com/api/dashboard/stats
```

---

## 👨‍💻 Author

**Harish**

This project was created as part of a Full-Stack Development Assignment, demonstrating proficiency in:

- ✅ **Frontend Development** - React, CSS, Responsive Design
- ✅ **Backend Development** - Node.js, Express, REST APIs
- ✅ **Database Design** - SQLite, SQL Queries
- ✅ **Authentication** - JWT Implementation
- ✅ **DevOps** - Cloud Deployment (Render, Netlify)

---

## 📄 License

MIT License - Feel free to use this project for learning purposes.

---

<div align="center">

### 🌟 Thank you for reviewing this project! 🌟

**Live Demo:** [https://fullstackww.netlify.app](https://fullstackww.netlify.app)

</div>
