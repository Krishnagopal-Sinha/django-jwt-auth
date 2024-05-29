## Authentication System using Django & JWT 

### Overview
This Django project implements user registration, login, and authentication using JSON Web Tokens (JWT). It includes views for user registration, login, retrieving user details, and logging out.

### Requirements
- Checkout (requirements.txt)[./requirements.txt].

### Installation

Follow these steps to get the project up and running on your local machine.

#### 1. Clone the Repository

```sh
git clone https://github.com/yourusername/django-jwt-auth.git
cd django-jwt-auth
```

#### 2. Create and Activate a Virtual Environment

```sh
python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

#### 3. Install the Required Python Packages

```sh
pip install -r requirements.txt
```

#### 5. Apply Migrations

```sh
python manage.py migrate
```

#### 6. Create a Superuser

```sh
python manage.py createsuperuser
```

#### 7. Run the Server

```sh
python manage.py runserver
```

Hopefully, any other issues can be debugged with help of internet.

### Running the Project

1. **Start the Django development server:**

```sh
python manage.py runserver
```

2. **Access the application:**

- Register a new user at `/api/register/`
- Log in at `/api/login/`
- View user details at `/api/user/`
- Log out at `/api/logout/`

### Notes

- Ensure the JWT secret key is kept secure and not hard-coded in the source code. Use environment variables for sensitive information.
- The JWT token is stored in an HTTP-only cookie to mitigate XSS attacks.
- This is a first draft thus, probably insecure in few ways, subject to change.
