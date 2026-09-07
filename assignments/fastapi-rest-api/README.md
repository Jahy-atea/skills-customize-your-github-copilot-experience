# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Build a REST API with FastAPI that serves and manages a small collection of books. Practice defining API routes, using path and request-body data, and returning appropriate HTTP responses.

## 📝 Tasks

### 🛠️ Create a Health Check Endpoint

#### Description
In `starter-code.py`, create a `GET /health` endpoint that confirms the API is running.

#### Requirements
Completed program should:

- Create a FastAPI application named `app`.
- Respond to `GET /health` with status code `200`.
- Return JSON in this format:
  ```json
  {"status": "ok"}
  ```

### 🛠️ Retrieve Books

#### Description
Add endpoints that let a client retrieve the complete book collection and look up one book by its ID.

#### Requirements
Completed program should:

- Respond to `GET /books` with the complete list of books.
- Respond to `GET /books/{book_id}` with the matching book.
- Return status code `404` and a helpful detail message when a requested book ID does not exist.
- Return each book with an `id`, `title`, and `author`.

### 🛠️ Add and Remove Books

#### Description
Extend the API so a client can add a book to the in-memory collection and remove a book by ID.

#### Requirements
Completed program should:

- Respond to `POST /books` and accept a JSON request body containing `title` and `author`.
- Assign each new book a unique integer `id` and return status code `201`.
- Respond to `DELETE /books/{book_id}` with status code `204` when a matching book is removed.
- Return status code `404` when the client tries to delete a book that does not exist.
