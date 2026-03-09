# API YamDB

RESTful API service for collecting user reviews on various types of media such as books, movies, music, and other works.

The project demonstrates backend development using **Django REST Framework**, including authentication, permissions, and relational data modeling.

---

# Project Description

**YamDB API** allows users to leave reviews and ratings for different works.

Users can:

- Leave reviews with a rating from **1 to 10**
- Comment on reviews
- View the **average rating** of works
- Browse categories and genres
- Manage data through an admin interface

Administrators can:

- Manage categories and genres
- Moderate reviews and comments
- Manage user roles and permissions

---

# Features

- JWT authentication
- Role-based access control (User / Moderator / Admin)
- Reviews and comments system
- Rating calculation
- API filtering and pagination
- CSV data import support
- Django admin panel

---

# Tech Stack

Backend:

- Python
- Django
- Django REST Framework

Tools:

- Git
- SQLite / PostgreSQL (depending on environment)

---

# Architecture

The application follows a typical Django REST architecture:


Client
↓
Django REST API
↓
Business Logic
↓
Django ORM
↓
Database


Main entities:

- Users
- Titles (works)
- Categories
- Genres
- Reviews
- Comments

---

# Installation

### 1 Clone repository

```bash
git clone git@github.com:your_profile/api_yamdb.git
cd api_yamdb
2 Create virtual environment

Linux / MacOS

python -m venv venv
source venv/bin/activate

Windows

python -m venv venv
venv\Scripts\activate
3 Install dependencies
pip install -r requirements.txt
4 Apply migrations
python manage.py migrate
5 Run server
python manage.py runserver

API will be available at:

http://127.0.0.1:8000
API Endpoints
Method	Endpoint	Description
GET	/api/v1/titles/	List of works
GET	/api/v1/titles/{id}/reviews/	List of reviews
POST	/api/v1/titles/{id}/reviews/	Create review
PATCH	/api/v1/reviews/{id}/	Update review
DELETE	/api/v1/reviews/{id}/	Delete review
Authentication

JWT authentication is used.

Get token:

POST /api/v1/auth/token/

Use token:

Authorization: Bearer <your_token>
Team
Ivan Safonov

User management system:

Registration and authentication

User permissions

Token management

Email confirmation

Kirill Serykh

Titles, genres, and categories:

Models

API endpoints

CSV data import

Ilya Fedorenko

Reviews and comments system:

Review models

Comment models

Rating calculation

Author

Ilya Fedorenko
