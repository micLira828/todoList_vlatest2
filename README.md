# 📝 Notes & Tasks API  
A clean, modern REST API for managing users, lists, and todos.  
Part of my full-stack developer portfolio.

---

## 📖 Overview

The Notes & Tasks API provides essential backend functionality for a basic productivity app.  
Users can sign up, log in, create task lists, and manage todos inside each list.

This project demonstrates:
- relational data modeling  
- authentication  
- full CRUD operations  
- organized project planning with Trello  
- professional API documentation  

---

## 🗂 Tech Stack

- **Node.js**
- **Express.js**
- **PostgreSQL**
- **JWT Authentication**
- **REST API Architecture**

---

## 🧠 Features

- User signup, login, logout  
- JWT-secured authentication  
- Create/update/delete task lists  
- Create/update/delete todos  
- Full relational structure (1 user → many lists → many todos)  
- Consistent error handling  

---

## 🔄 Kanban Workflow (Trello)

This project uses a Trello Kanban board to plan and track development progress.

🔗 **Trello Board:** *(insert link here)*

### 📌 Screenshot  
*(Upload `kanban.png` and uncomment the line below)*

<!-- ![Kanban Board](./kanban.png) -->

---

## 🏗 Database Schema

Designed using dbdiagram.io.

### 📌 Screenshot  
*(Upload `schema.png` and uncomment the line below)*

<!-- ![Database Schema](./schema.png) -->

### Schema Overview
- **Users**  
  - id, email, username, password_hash  
- **Lists**  
  - id, user_id, title  
- **Todos**  
  - id, list_id, text, is_completed  

---

## 📁 Project Structure



## 🚀 Getting Started

### 1. Clone the repo

### 2. Install dependencies


### 3. Add environment variables
Create `.env`:


### 4. Start development server  

---

# 🧪 API Endpoints

Below is the full endpoint list for your **new** Notes/Tasks API design.

---

## 🔐 Authentication

### **POST /auth/signup**  
Create a new user account.

### **POST /auth/login**  
Authenticate and receive a JWT.

### **POST /auth/logout**  
Invalidate user session (client-side token removal).

### **GET /auth/me**  
Return the authenticated user.

---

## 📋 Lists

### **POST /lists**  
Create a new list for the logged-in user.

### **GET /lists**  
Get all lists belonging to the logged-in user.

### **GET /lists/:id**  
Get a single list by ID.

### **PUT /lists/:id**  
Update a list’s title.

### **DELETE /lists/:id**  
Delete a list and all its todos.

---

## ✅ Todos

### **POST /lists/:listId/todos**  
Create a todo under a specific list.

### **GET /lists/:listId/todos**  
Get all todos for a list.

### **PUT /todos/:id**  
Update a todo (text or completion status).

### **DELETE /todos/:id**  
Remove a todo.

---

## ❌ Error Handling

Standardized JSON error structure:


---

## 🧩 Planning Files

This repo includes the full planning assets:

- `schema.dbdiagram.txt` — ERD schema  
- `tasks.csv` — Trello Kanban import file  

---

## ✨ Author

**Michelle Liran Gepshtein**  
Digital Alchemist • Full-Stack Developer


