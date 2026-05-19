# NOVA E-Commerce Store 🛍️
Full-stack e-commerce application built with Django (backend) + HTML/CSS/JS (frontend).

## Project Structure
```
ecommerce/
├── backend/          # Django backend
│   ├── ecommerce_backend/  # Django project settings & URLs
│   ├── store/              # Main app (models, views, serializers)
│   ├── db.sqlite3          # SQLite database (auto-created)
│   └── manage.py
├── frontend/
│   └── index.html          # Complete single-page frontend
└── README.md
```

## Quick Start

### 1. Install Dependencies
```bash
cd backend
pip install -r requirements.txt
```

### 2. Run Migrations & Seed Data
```bash
python manage.py migrate
python manage.py seed_data
```

### 3. Start Backend Server
```bash
python manage.py runserver
```
Backend runs at: http://localhost:8000

### 4. Open Frontend
Open `frontend/index.html` in your browser (or serve with Live Server).

## Default Admin Credentials
- Username: `admin`
- Password: `admin123`
- Admin Panel: http://localhost:8000/admin/

## API Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| POST | /api/auth/register/ | Register new user | No |
| POST | /api/auth/login/ | Login & get token | No |
| POST | /api/auth/logout/ | Logout | Yes |
| GET | /api/auth/profile/ | Get profile | Yes |
| GET | /api/categories/ | List categories | No |
| GET | /api/products/ | List products (filter: ?search=, ?category=) | No |
| GET | /api/products/{id}/ | Product details | No |
| GET/POST/PUT/DELETE | /api/cart/ | Manage cart | Yes |
| GET/POST | /api/orders/ | List/create orders | Yes |
| GET | /api/orders/{id}/ | Order details | Yes |

## Features
- ✅ User Registration & Login (Token auth)
- ✅ Product listing with search & category filter
- ✅ Product detail page with quantity control
- ✅ Shopping cart (add, update, remove)
- ✅ Checkout with shipping address
- ✅ Order history tracking
- ✅ Django Admin panel for managing products/orders
- ✅ SQLite database (no setup required)
- ✅ CORS enabled for frontend

## Tech Stack
- **Backend**: Django 4.2, Django REST Framework, SQLite
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Auth**: Token-based authentication (DRF)
- **CORS**: django-cors-headers
