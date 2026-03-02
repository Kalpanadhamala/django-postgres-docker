# Django Books API

A simple Django REST API for Books CRUD operations.

## Setup

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Create PostgreSQL database:
```sql
CREATE DATABASE books_db;
```

3. Update `.env` file with your database credentials.

4. Run migrations:
```bash
python manage.py migrate
```

5. Run the server:
```bash
python manage.py runserver
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/books/` | List all books |
| POST | `/api/books/` | Create a new book |
| GET | `/api/books/<id>/` | Get a specific book |
| PUT | `/api/books/<id>/` | Update a book |
| PATCH | `/api/books/<id>/` | Partial update a book |
| DELETE | `/api/books/<id>/` | Delete a book |

## Example Usage

### Create a book
```bash
curl -X POST http://localhost:8000/api/books/ \
  -H "Content-Type: application/json" \
  -d '{"name": "My Book", "description": "A great book"}'
```

### List all books
```bash
curl http://localhost:8000/api/books/
```

### Get a single book
```bash
curl http://localhost:8000/api/books/1/
```

### Update a book
```bash
curl -X PUT http://localhost:8000/api/books/1/ \
  -H "Content-Type: application/json" \
  -d '{"name": "Updated Book", "description": "Updated description"}'
```

### Delete a book
```bash
curl -X DELETE http://localhost:8000/api/books/1/
```
