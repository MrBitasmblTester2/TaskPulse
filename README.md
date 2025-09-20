# TaskPulse — Web-Based Task Management Application

Description
TaskPulse is a web-based task management app where users can add, edit, and delete tasks. The app supports user authentication using JWT, categorizes tasks by project, and displays tasks with priority sorting.

## Tech Stack
- React
- Node.js
- Express
- jsonwebtoken

## Requirements
- Implement JWT authentication for secure routes (use jsonwebtoken and store JWT_SECRET in environment variable)
- Protect API endpoints with auth middleware (mount auth middleware before task routes)
- Design RESTful API for tasks (CRUD) using Express Router and HTTP verbs
- Implement task categorization and priority sorting (use array sort and include project categories in task model)
- Build React components for login and task display (store JWT in localStorage and include in Authorization header)
- Adhere to coding best practices and modular structure (organize code into modules, use linting tools)

## Installation
1. Clone the repository:
   git clone <repo-url>
2. Navigate to the project directory:
   cd TaskPulse

### Backend setup
3. Navigate to server directory and install dependencies:
   cd server
   npm install
4. Create a .env file in the server root and add:
   JWT_SECRET=your_jwt_secret
5. Start the backend server:
   npm run dev

### Frontend setup
6. Navigate to client directory and install dependencies:
   cd ../client
   npm install
7. Start the frontend application:
   npm start

## Usage
- Register or log in via the React app
- After login, JWT is stored in localStorage under 'token'
- The app displays tasks fetched from protected API endpoints with project categorization and priority sorting
- Use the UI to add, edit, or delete tasks within projects

## Implementation Steps
1. Initialize a Node.js project and install Express and jsonwebtoken
2. Create Express server and configure middleware (bodyParser, cors)
3. Define auth routes for user registration and login using JWT
4. Implement auth middleware to verify JWT_SECRET on protected routes
5. Design Task model to include title, description, project, and priority fields
6. Build RESTful task routes (CRUD) using Express Router and mount auth middleware before them
7. Initialize React app with Create React App
8. Implement login and protected routing in React, storing JWT in localStorage
9. Create TaskList and TaskForm components to display and manage tasks
10. Integrate frontend with backend API using fetch or axios and include Authorization header

## API Endpoints
- POST /api/auth/register: Register a new user
- POST /api/auth/login: Authenticate user and receive a JWT
- GET /api/tasks: Retrieve all tasks (protected)
- POST /api/tasks: Create a new task (protected)
- GET /api/tasks/:id: Retrieve a specific task by ID (protected)
- PUT /api/tasks/:id: Update a task by ID (protected)
- DELETE /api/tasks/:id: Delete a task by ID (protected)