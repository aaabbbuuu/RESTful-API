# SecureAPIProject

This project demonstrates how to build a secure RESTful API using Django, Django REST framework, and JWT authentication. The API includes user registration, login, and role-based access control.

## Features

- User registration
- User login with JWT authentication
- Role-based access control

## Setup

### Prerequisites

- Python 3.8+
- pip

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/SecureAPIProject.git
    cd SecureAPIProject
    ```

2. Create and activate a virtual environment:

    ```bash
    python -m venv secureapi_env
    secureapi_env\Scripts\activate  # On Windows
    # source secureapi_env/bin/activate  # On Unix or MacOS
    ```

3. Install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Apply migrations:

    ```bash
    python manage.py makemigrations
    python manage.py migrate
    ```

5. Create a superuser:

    ```bash
    python manage.py createsuperuser
    ```

6. Run the development server:

    ```bash
    python manage.py runserver
    ```

7. Access the API at `http://127.0.0.1:8000/`.

## API Endpoints

### Register

- URL: `/api/register/`
- Method: `POST`
- Body:
    ```json
    {
        "username": "exampleuser",
        "email": "exampleuser@example.com",
        "password": "examplepassword123"
    }
    ```

### Login

- URL: `/api/login/`
- Method: `POST`
- Body:
    ```json
    {
        "username": "exampleuser",
        "password": "examplepassword123"
    }
    ```

### Refresh Token

- URL: `/api/token/refresh/`
- Method: `POST`
- Body:
    ```json
    {
        "refresh": "your-refresh-token"
    }
    ```

## License

This project is licensed under the MIT License.
