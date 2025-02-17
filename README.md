# Task Manager (Backend)

## Overview
The **Task Manager** is a simple server-based backend project built using **Node.js** and **Express.js**. It allows users to create and manage tasks, storing them in real-time as `.txt` files using the **FS (File System) module**. Each task is saved as a separate text file containing its details.

## Features
- Create new tasks dynamically.
- Store task details in individual `.txt` files.
- Retrieve stored tasks.
- Delete tasks when no longer needed.
- Uses **Node.js** and **Express.js** for backend API.
- Real-time file creation with **fs** module.

## Technologies Used
- **Node.js** - JavaScript runtime for backend.
- **Express.js** - Framework for building RESTful APIs.
- **FS (File System) module** - Handles file operations.

## Installation & Setup

### Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v14 or later)

### Clone the Repository
```sh
git clone https://github.com/your-username/task-manager.git
cd task-manager
```

### Install Dependencies
```sh
npm install
```

### Run the Server
```sh
node server.js
```
The server will run on `http://localhost:3000/` (default port).

## API Endpoints

### 1. Create a Task
**Endpoint:** `POST /task`

**Request Body (JSON):**
```json
{
  "title": "Task Title",
  "description": "Task description goes here"
}
```

**Response:**
```json
{
  "message": "Task created successfully",
  "filename": "task-17082024.txt"
}
```
A `.txt` file containing the task details will be created in the `/tasks` directory.

### 2. Get All Tasks
**Endpoint:** `GET /tasks`

**Response:**
```json
[
  "task-17082024.txt",
  "task-17082025.txt"
]
```
Lists all task files available in the `/tasks` directory.

### 3. Get Task by Filename
**Endpoint:** `GET /task/:filename`

**Example:** `GET /task/task-17082024.txt`

**Response:**
```
Title: Task Title
Description: Task description goes here
```

### 4. Delete a Task
**Endpoint:** `DELETE /task/:filename`

**Example:** `DELETE /task/task-17082024.txt`

**Response:**
```json
{
  "message": "Task deleted successfully"
}
```

## Project Structure
```
/task-manager
│── tasks/                  # Stores created task files
│── server.js               # Main server file
│── package.json            # Dependencies and scripts
│── README.md               # Documentation
```

## Future Improvements
- Add **task updating** functionality.
- Implement **task categories**.
- Integrate with a **database** for better storage.

## License
This project is licensed under the **MIT License**.

## Author
Developed by **Rajnish Sharma** - Founder, Rixi Lab.

---

Feel free to **contribute** or **raise issues** if you have suggestions!

