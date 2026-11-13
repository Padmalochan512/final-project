# Final Project

A full-stack restaurant application built with a React frontend and a Django REST API backend. The project includes user authentication, contact management, blog content, and restaurant menu functionality.

## Project Overview

This repository is structured as a monorepo-style application with two main components:

- `restaurants/client` — React + Vite frontend
- `restaurants/server` — Django + DRF backend

## Tech Stack

### Frontend
- React 19
- Vite
- React Router
- Tailwind CSS
- Axios
- Lucide React

### Backend
- Python
- Django
- Django REST Framework
- SQLite database
- Django CORS Headers

## Repository Structure

```text
final-project/
├── README.md
├── restaurants/
│   ├── client/
│   │   ├── .env
│   │   ├── .gitignore
│   │   ├── .oxlintrc.json
│   │   ├── index.html
│   │   ├── package.json
│   │   ├── package-lock.json
│   │   ├── vite.config.js
│   │   ├── vercel.json
│   │   ├── public/
│   │   └── src/
│   │       ├── assets/
│   │       ├── components/
│   │       ├── pages/
│   │       ├── routes/
│   │       ├── App.css
│   │       ├── App.jsx
│   │       ├── index.css
│   │       └── main.jsx
│   └── server/
│       ├── api/
│       │   ├── migrations/
│       │   ├── admin.py
│       │   ├── apps.py
│       │   ├── models.py
│       │   ├── serializers.py
│       │   ├── tests.py
│       │   ├── views.py
│       │   └── __init__.py
│       ├── server/
│       │   ├── __init__.py
│       │   ├── asgi.py
│       │   ├── settings.py
│       │   ├── urls.py
│       │   ├── wsgi.py
│       │   └── __pycache__/
│       ├── db.sqlite3
│       ├── manage.py
│       ├── requirements.txt
│       └── __pycache__/
└── restaurants.zip
```

## Features

- User login and registration
- Contact management APIs
- Blog listing and CRUD operations
- Menu retrieval and detail views
- Responsive frontend navigation and layout
- Separate frontend/backend deployment readiness

## Backend API Highlights

The Django server exposes endpoints such as:

- `POST /login/`
- `POST /register/`
- `GET /contacts/`
- `POST /contacts/create/`
- `GET /contacts/<id>/`
- `PUT /contacts/<id>/update/`
- `DELETE /contacts/<id>/delete/`
- `GET /blogs/`
- `POST /blogs/create/`
- `GET /menu/`
- `GET /menu/<id>/`

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Padmalochan512/final-project.git
cd final-project
```

### 2. Setup the frontend

```bash
cd restaurants/client
npm install
npm run dev
```

### 3. Setup the backend

```bash
cd ../server
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

## Environment Configuration

The frontend uses a `.env` file in `restaurants/client`.

```env
VITE_BASE_URL=https://final-project-1-uks9.onrender.com
```

Update this value if you are running the backend locally or on a different deployment target.

## Development Notes

- Frontend is powered by Vite and is structured around reusable components, pages, and route-based navigation.
- Backend is built with Django and exposes REST endpoints consumed by the client application.
- SQLite is used as the default database for development.

## License

This project is currently provided for academic / project use. Add a formal license if you plan to distribute it publicly.

## Contributors

- Padmalochan512

## Status

This repository contains a working full-stack restaurant project with frontend and backend integration, ready for further development, polishing, and deployment.
