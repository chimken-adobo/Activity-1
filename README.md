# 🧩 To-Do List App — Full Stack (React + NestJS)

This is a **full-stack To-Do List App** consisting of:
- A **frontend** built with **React (Create React App)** and styled using **custom CSS** with glassmorphism and gradients.  
- A **backend** built with **NestJS** and **TypeORM**, using **SQLite** for local data storage.  

The app provides complete **CRUD functionality** — create, read, update, and delete tasks — with a clean UI and a RESTful API.

---

## 🚀 Features

### Frontend
- Add, edit, check/uncheck, and delete tasks  
- Animated gradient background  
- Glassmorphism card design  
- Connects to backend via **Axios**

### Backend
- Full CRUD API for task management  
- Built with **NestJS** (scalable Node.js framework)  
- **SQLite** database (auto-created)  
- API documentation via **Swagger UI**

---

## 🧰 Requirements

Before you begin, make sure you have:

- **Node.js** (>= 18.x recommended)  
- **npm** (comes with Node.js)  
- *(Optional)* **NestJS CLI** for development:
  ```bash
  npm install -g @nestjs/cli
  ```

---

## ⚙️ Installation & Setup (For a New Device)

### 1. Clone the repository
```bash
git clone https://github.com/chimken-adobo/Activity-1.git
cd Activity-1
```

---

### 2. Setup the Backend (NestJS API)
```bash
cd backend
npm install
npm run start:dev
```

- Runs the server at:  
  ```
  http://localhost:3000
  ```
- The SQLite database file is created automatically.  
- You can check API docs (if enabled) at:
  ```
  http://localhost:3000/api
  ```

---

### 3. Setup the Frontend (React App)
Open a **new terminal**, then run:
```bash
cd frontend
npm install
npm start
```

- Runs the app at:  
  ```
  http://localhost:3001
  ```

⚠️ **Important:**  
If your backend is running on port `3000`, make sure the frontend is on a **different port** (`3001` or higher).  
To connect them properly, set this proxy in the frontend’s `package.json`:

```json
"proxy": "http://localhost:3000"
```

This allows the frontend to automatically send API requests to the backend.

---

## 📁 Project Structure

```
Activity-1/
├── backend/              # NestJS backend
│   ├── src/
│   │   ├── tasks/         # Task module (controller, service, entity)
│   │   ├── app.module.ts  # Root module
│   │   └── main.ts        # Entry point
│   ├── package.json
│   └── ...
│
└── frontend/             # React frontend
    ├── src/
    │   ├── App.js         # Main app component
    │   ├── App.css        # Styles (gradient + glassmorphism)
    │   ├── index.js       # Entry point
    │   └── components/    # Reusable UI components
    ├── package.json
    └── ...
```

---

## 🧠 Example Usage

1. **Start the backend** → `npm run start:dev` inside `backend/`  
2. **Start the frontend** → `npm start` inside `frontend/`  
3. Add a new task using the input field  
4. Edit or delete tasks as needed  
5. Check/uncheck to mark completion  

---

## 🧩 Available Scripts

### Frontend (React)
| Command | Description |
|----------|-------------|
| `npm start` | Start the React app (dev mode) |

### Backend (NestJS)
| Command | Description |
|----------|-------------|
| `npm run start` | Start the server (normal mode) |
| `npm run start:dev` | Start in watch mode (dev) |

---

## 🧾 Example API Endpoints

| Method | Endpoint | Description |
|---------|-----------|-------------|
| GET | `/tasks` | Fetch all tasks |
| POST | `/tasks` | Create a new task |
| PUT | `/tasks/:id` | Update a task |
| DELETE | `/tasks/:id` | Delete a task |
