# Bitasmbl-TaskForge

A secure web-based task management application built with Node.js and React, featuring JWT-based user authentication, project-focused task categorization, priority-driven sorting, and full CRUD operations.

## Tech Stack
- Node.js
- React

## Requirements
- Implement user authentication with JWT (Hint: Store tokens securely, e.g., HttpOnly cookies)
- Build RESTful CRUD endpoints for tasks (Hint: Use appropriate HTTP methods and status codes)
- Develop React components for login and task management UI (Hint: Manage auth and task state with React hooks)

## Installation
1. Clone the repository:
   bash
   git clone https://github.com/your-username/Bitasmbl-TaskForge.git
   
2. Install backend dependencies:
   bash
   cd Bitasmbl-TaskForge/server
   npm install
   
3. Install frontend dependencies:
   bash
   cd ../client
   npm install
   
4. Configure environment variables:
   **Server** (`server/.env`):
   bash
   JWT_SECRET=your_jwt_secret
   PORT=5000
   
   **Client** (`client/.env`):
   bash
   REACT_APP_API_URL=http://localhost:5000/api
   

## Usage
1. Start the backend server:
   bash
   cd server
   npm run dev
   
2. Start the frontend development server:
   bash
   cd client
   npm start
   
3. Open your browser at http://localhost:3000 to access the application. Log in to manage your tasks.

## Implementation Steps
1. Initialize a Node.js backend and install Express to serve RESTful endpoints under `/api`.
2. Implement JWT-based authentication: generate tokens on login, store them in HttpOnly cookies, and protect routes with middleware.
3. Define a Task model and create RESTful CRUD routes: `GET /tasks`, `POST /tasks`, `GET /tasks/:id`, `PUT /tasks/:id`, `DELETE /tasks/:id`.
4. Scaffold the React frontend using Create React App and configure routing for authentication and task management.
5. Develop React components (`LoginForm`, `TaskList`, `TaskForm`, `TaskItem`) and manage state with React hooks.
6. Build API service utilities to handle HTTP requests, automatically including JWT credentials from cookies.
7. Add project-focused task categorization and priority-driven sorting features in the UI.

## API Endpoints
- POST /api/auth/login: Authenticate user and set JWT in HttpOnly cookie
- GET /api/tasks: Retrieve all tasks for the authenticated user
- GET /api/tasks/:id: Retrieve a specific task by ID
- POST /api/tasks: Create a new task
- PUT /api/tasks/:id: Update an existing task
- DELETE /api/tasks/:id: Delete a task