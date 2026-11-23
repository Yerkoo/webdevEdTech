# EdTech — Online Course Platform

A fullstack web platform for publishing, searching and watching online courses. The client is an Angular SPA, the server is a REST API built with Django REST Framework.

## Features

- **Course catalog** — all courses shown as cards
- **Filtering** — by category (Programming, Math, Languages, etc.) and a "My Courses" tab
- **Author dashboard** — create a course with a cover preview and an embedded YouTube video
- **Reviews** — comment on courses and rate them from 1 to 5 stars
- **Wishlist** — save courses to your personal favorites
- **Authentication** — JWT (SimpleJWT) with token blacklisting; an Angular HTTP interceptor catches expired tokens and redirects to the login page

## Tech Stack

| Layer | Technologies |
| --- | --- |
| Frontend | Angular 21 (standalone components, Signals), TypeScript, RxJS, HTML/CSS (Flexbox/Grid) |
| Backend | Python 3, Django, Django REST Framework, SimpleJWT, django-cors-headers |
| Database | SQLite |
| API testing | Postman collections (`postman/`) |

## Project Structure

```
backend/    Django REST API (apps: courses, users)
frontend/   Angular client
postman/    Postman collections for the API
```

## Running Locally

Both servers must be running at the same time.

### Backend

```bash
cd backend
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

API: http://127.0.0.1:8000/

### Frontend

```bash
cd frontend
npm install
npx ng serve
```

App: http://localhost:4200/
