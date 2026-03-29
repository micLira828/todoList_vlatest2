# Todo App 


## 🔌 API Docs

## Lists

### GET /lists
```json
[
  {
    "id": 1,
    "name": "Work",
    "description": "Work tasks",
    "created_at": "2026-01-01",
    "updated_at": "2026-01-02"
  }
]
```

### GET /lists/:listId
```json
{
  "id": 1,
  "name": "Work",
  "description": "Work tasks",
  "created_at": "2026-01-01",
  "updated_at": "2026-01-02"
}
```

### POST /lists
```json
{
  "name": "Work",
  "description": "Work tasks"
}
```

Response:
```json
{
  "message": "List created successfully",
  "list": {
    "id": 1,
    "name": "Work",
    "description": "Work tasks",
    "created_at": "2026-01-01",
    "updated_at": "2026-01-02"
  }
}
```

### PUT /lists/:listId
```json
{
  "name": "Updated list",
  "description": "Updated description"
}
```

Response:
```json
{
  "message": "List updated successfully",
  "list": {
    "id": 1,
    "name": "Updated list",
    "description": "Updated description",
    "created_at": "2026-01-01",
    "updated_at": "2026-01-02"
  }
}
```

### DELETE /lists/:listId
```json
{
  "status": 200,
  "message": "List deleted successfully"
}
```

---

## Todos in a List

### GET /lists/:listId/todos
```json
{
  "list": {
    "id": 1,
    "name": "Work",
    "description": "Work tasks",
    "created_at": "2026-01-01",
    "updated_at": "2026-01-02"
  },
  "todos": [
    {
      "id": 1,
      "name": "Finish report",
      "due_date": "2026-01-05",
      "priority": "high",
      "description": "Complete the final report",
      "created_at": "2026-01-01",
      "updated_at": "2026-01-02"
    }
  ]
}
```

---

## Single Todo

### GET /todos/:todoId
```json
{
  "id": 1,
  "name": "Finish report",
  "due_date": "2026-01-05",
  "priority": "high",
  "description": "Complete the final report",
  "created_at": "2026-01-01",
  "updated_at": "2026-01-02"
}
```

### POST /todos
```json
{
  "name": "Finish report",
  "due_date": "2026-01-05",
  "priority": "high",
  "description": "Complete the final report"
}
```

Response:
```json
{
  "message": "Todo created successfully",
  "todo": {
    "id": 1,
    "name": "Finish report",
    "due_date": "2026-01-05",
    "priority": "high",
    "description": "Complete the final report",
    "created_at": "2026-01-01",
    "updated_at": "2026-01-02"
  }
}
```

### PUT /todos/:todoId
```json
{
  "name": "Updated task",
  "due_date": "2026-01-06",
  "priority": "medium",
  "description": "Updated description"
}
```

Response:
```json
{
  "message": "Todo updated successfully",
  "todo": {
    "id": 1,
    "name": "Updated task",
    "due_date": "2026-01-06",
    "priority": "medium",
    "description": "Updated description",
    "created_at": "2026-01-01",
    "updated_at": "2026-01-02"
  }
}
```

### DELETE /todos/:todoId
```json
{
  "status": 200,
  "message": "Todo deleted successfully"
}
```

---

## Optional Relationship Routes

### POST /lists/:listId/todos/:todoId
```json
{
  "message": "Todo added to list successfully"
}
```

### DELETE /lists/:listId/todos/:todoId
```json
{
  "message": "Todo removed from list successfully"
}
```
