# My Todo App 🗒️

A clean, testable backend web application built with FastAPI, SQLAlchemy, and Alembic. This project demonstrates practical backend development with a modular structure, database migrations, templating, and automated testing — ready for real-world extensions.

---

## Table of Contents

* [About This Project](#about-this-project)
* [Features](#features)
* [Tech Stack](#tech-stack)
* [Getting Started](#getting-started)

  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
  * [Database Setup](#database-setup)
  * [Running the App](#running-the-app)
* [API Endpoints](#api-endpoints)
* [Testing](#testing)
* [Project Structure](#project-structure)
* [Responsibilities & Focus Areas](#responsibilities--focus-areas)
* [Future Improvements](#future-improvements)
* [License](#license)
* [Contact](#contact)

---

## About This Project

This todo app was developed as a compact, production-style backend project using FastAPI and SQLAlchemy. It focuses on clean architecture, maintainability, and full CRUD functionality through both RESTful APIs and a web interface.

The project demonstrates backend skills that apply across business logic systems, admin tools, and data-centric or AI-powered applications.

---

## Features

* Create, view, edit, and delete todos
* RESTful API with JSON-based endpoints
* Web interface using Jinja templates
* Alembic-powered schema migrations
* SQLite as default database (easily switchable)
* Unit testing with `pytest`

---

## Tech Stack

* **Backend**: FastAPI
* **ORM**: SQLAlchemy
* **Migrations**: Alembic
* **Templating**: Jinja2
* **Database**: SQLite (default)
* **Testing**: pytest

---

## Getting Started

### Prerequisites

* Python 3.10+
* `virtualenv` or `venv`

### Installation

```bash
git clone https://github.com/ErmisCho/my-todo-app.git
cd my-todo-app
python -m venv .env
source .env/bin/activate       # or .env\Scripts\activate on Windows
pip install -r requirements.txt
```

### Database Setup

```bash
alembic upgrade head
```

### Running the App

```bash
uvicorn main:app --reload
```

* App: `http://127.0.0.1:8000`
* Swagger Docs: `http://127.0.0.1:8000/docs`
* ReDoc: `http://127.0.0.1:8000/redoc`

---

## API Endpoints

| Method | Path              | Description               |
| ------ | ----------------- | ------------------------- |
| GET    | `/api/todos/`     | Get all todos             |
| GET    | `/api/todos/{id}` | Get a specific todo by ID |
| POST   | `/api/todos/`     | Create a new todo         |
| PUT    | `/api/todos/{id}` | Update a todo             |
| DELETE | `/api/todos/{id}` | Delete a todo             |

---

## Testing

Run the test suite using:

```bash
pytest
```

Tests run in isolation using a dedicated SQLite test database (`testdb.db`).

---

## Project Structure

```
.
├── alembic/              # Database migration scripts
├── routers/              # API route logic
├── static/               # Static assets (CSS, JS, etc.)
├── templates/            # Jinja2 HTML templates
├── test/                 # Unit tests with pytest
├── alembic.ini           # Alembic configuration
├── database.py           # DB session setup
├── main.py               # FastAPI app entrypoint
├── models.py             # ORM models
├── requirements.txt      # Dependencies
├── todosapp.db           # Main SQLite database
└── testdb.db             # Test database
```

---

## Responsibilities & Focus Areas

* Designed and implemented a modular FastAPI backend using best practices
* Managed database schema changes via Alembic migrations
* Developed and tested API endpoints with full CRUD logic
* Integrated Jinja templates to support browser-based interaction
* Wrote automated test cases with `pytest` to ensure correctness and prevent regressions
* Built a foundation applicable to both business-logic and data-driven systems

---

## Future Improvements

* Add authentication (session- or JWT-based)
* Migrate from SQLite to PostgreSQL for production environments
* Dockerize the application for containerized deployment
* Add ML-based task prioritization using scikit-learn
* Introduce pagination and filtering for API endpoints
* Add logging and centralized error handling
