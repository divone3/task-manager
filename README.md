Task Manager API

  A simple Task Manager backend built with Django & Django REST Framework.
  Perfect for demonstrating user authentication, CRUD operations, and API skills for your GitHub portfolio.

Live Demo

  Register: /api/register/
  
  Login: /api-auth/login/
  
  Task API: /api/tasks/

Features

  User registration & login/logout (Session Authentication)
  
  Create, Read, Update, Delete tasks
  
  Each task linked to logged-in user
  
  RESTful API endpoints with Django REST Framework

Tech Stack

  Python 3.11+
  
  Django 6+
  
  Django REST Framework
  
  SQLite (default, can be swapped for PostgreSQL)
  
  Gunicorn (for deployment)

Installation

  Clone the repository:

    git clone https://github.com/<username>/task-manager.git
    cd task-manager


  Create virtual environment and install dependencies:

    python -m venv venv
    source venv/bin/activate   # Linux/Mac
    venv\Scripts\activate      # Windows
    pip install -r requirements.txt


  Run migrations:

    python manage.py migrate


  Run the server:

    python manage.py runserver


  Open in browser:

    Register: http://127.0.0.1:8000/api/register/
    
    Login: http://127.0.0.1:8000/api-auth/login/
    
    Task API: http://127.0.0.1:8000/api/tasks/

API Examples

  Register
    
    POST /api/register/
    {
      "username": "your_username",
      "password": "your_password"
    }


  Tasks

    GET /api/tasks/
    POST /api/tasks/ { "title": "Learn Django", "description": "Finish project", "status": "todo" }
    PUT /api/tasks/<id>/ { ... }
    DELETE /api/tasks/<id>/

Folder Structure
  TaskManager/
  ├── TaskManager/      # Django project settings
  ├── tasks/            # Task app
  │   ├── models.py
  │   ├── serializers.py
  │   ├── views.py
  │   └── urls.py
  ├── db.sqlite3
  ├── manage.py
  ├── requirements.txt
  └── README.md

Deployment

  Deployed on Heroku

  heroku run python manage.py migrate to set up database

  Access endpoints with browser session authentication

License

  MIT License © 2025
