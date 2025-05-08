# SecureAPIProject

A modern, secure RESTful API using Django 5, Django REST Framework, JWT auth, and environment-based configuration.

## 🚀 Features

- JWT Authentication (access + refresh tokens)
- Role-based access control
- Secure secret management via `.env`
- CORS support
- Environment-ready for production

## 🔧 Setup

### Prerequisites

- Python 3.8+
- pip

### Installation

```bash
git clone https://github.com/your-username/SecureAPIProject.git
cd SecureAPIProject
python -m venv venv
venv\Scripts\activate     # On Windows
# source venv/bin/activate  # On Unix/MacOS
pip install -r requirements.txt
```

Create a `.env` file:

```env
DJANGO_SECRET_KEY=your-secret-key
DJANGO_DEBUG=True
DJANGO_ALLOWED_HOSTS=localhost,127.0.0.1
```

Run migrations and create superuser:

```bash
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
```

Run the server:

```bash
python manage.py runserver
```

## 🔑 API Auth Endpoints

| Endpoint           | Method | Description         |
|--------------------|--------|---------------------|
| /api/register/     | POST   | Register a new user |
| /api/login/        | POST   | Login and get tokens |
| /api/token/refresh/| POST   | Refresh JWT token    |

## 🛡 Deployment

Use `gunicorn` in production:

```bash
gunicorn SecureAPIProject.wsgi:application --bind 0.0.0.0:8000
```

## 📄 License

MIT License