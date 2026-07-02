# Online Voting System [Update]

An online polling and voting system built with Django, designed to facilitate secure and efficient electronic voting for organizations and institutions.

## 📋 Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Configuration](#configuration)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

- **User Authentication**: Secure login system with email-based authentication
- **Custom User Model**: Flexible user management system
- **Role-Based Access**: Support for different user roles (voters, administrators)
- **Voting Management**: Create, manage, and conduct elections/polls
- **Results Dashboard**: View voting results and statistics
- **Admin Panel**: Complete administrative interface for managing elections
- **OTP Support**: Optional One-Time Password verification for enhanced security
- **Responsive Design**: Bootstrap-based responsive UI for all devices

## 🗂️ Project Structure

```
OnlineVoting-Django/
├── account/                    # User authentication and account management
│   ├── email_backend.py       # Custom email authentication backend
│   ├── forms.py               # User forms (registration, login)
│   ├── models.py              # Custom user model
│   └── middleware.py          # Custom middleware
├── voting/                     # Voting and election management
│   ├── models.py              # Voting models
│   ├── views.py               # Voting views
│   └── templates/             # Voting templates
├── administrator/             # Admin dashboard and management
│   ├── views.py               # Admin views
│   └── templates/             # Admin templates
├── e_voting/                  # Project settings and configuration
│   ├── settings.py            # Django settings
│   ├── urls.py                # URL routing
│   ├── wsgi.py                # WSGI configuration
│   └── asgi.py                # ASGI configuration
├── static/                    # Static files (CSS, JavaScript, images)
│   ├── css/                   # CSS files
│   ├── js/                    # JavaScript files
│   └── images/                # Images and assets
├── media/                     # User-uploaded files
├── manage.py                  # Django management script
└── election_title.txt         # Current election title configuration
```

## 🛠️ Technologies Used

- **Backend**: Django 3.1.7
- **Database**: SQLite3 (configurable to MySQL)
- **Frontend**: Bootstrap 3.3.7, HTML5, CSS3, JavaScript
- **Authentication**: Django authentication with email backend
- **Server**: WSGI/ASGI compatible

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.8 or higher
- pip (Python package manager)
- Virtual environment (recommended)
- Git

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/amithadityacp/Online-voting-System-.git
cd Online-voting-System-
```

### 2. Navigate to Project Directory

```bash
cd OnlineVoting-Django
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

### 4. Activate Virtual Environment

**On Windows:**
```bash
venv\Scripts\activate
```

**On macOS/Linux:**
```bash
source venv/bin/activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

## ⚙️ Setup Instructions

### 1. Make Database Migrations

```bash
python manage.py makemigrations
```

### 2. Apply Migrations

```bash
python manage.py migrate
```

### 3. Create a Superuser (Admin Account)

```bash
python manage.py createsuperuser
```

Follow the prompts to create an admin account with:
- Username
- Email
- Password

### 4. Run the Development Server

```bash
python manage.py runserver
```

The application will be available at `http://127.0.0.1:8000/`

## 📖 Usage

### Accessing the Application

1. **User Registration**: Navigate to the registration page and create a new account
2. **User Login**: Log in with your email and password
3. **Vote**: Participate in ongoing elections/polls
4. **Admin Dashboard**: Access the admin interface at `/admin/` with superuser credentials
5. **View Results**: Check voting results and statistics

### Setting Election Title

Edit the `election_title.txt` file to set the current election title:

```
Your Election Title Here
```

### Configuring OTP

In `e_voting/settings.py`, you can enable or disable OTP verification:

```python
SEND_OTP = False  # Set to True to enable OTP
```

When `SEND_OTP` is False, use `0000` as the default OTP for testing.

## 🔧 Configuration

### Database Configuration

**SQLite (Default):**
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}
```

**MySQL (Optional):**
Uncomment the MySQL configuration in `e_voting/settings.py`:
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'e_voting',
        'HOST': '127.0.0.1',
        'USER': 'root',
        'PASSWORD': ''
    }
}
```

### Email Configuration

Update the email backend settings in `settings.py` for sending OTPs and notifications:

```python
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'your-email-provider'
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = 'your-email@example.com'
EMAIL_HOST_PASSWORD = 'your-password'
```

### Debug Mode

For production, set DEBUG to False:
```python
DEBUG = False
ALLOWED_HOSTS = ['your-domain.com']
```

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is available on [CodeAstro](https://codeastro.com). Please refer to the LICENSE file for more information.

## 👨‍💻 Original Developer

Developed by **Owonubi Job Sunday**

For more projects, visit [CodeAstro](https://codeastro.com)

## 📞 Support

For issues, questions, or suggestions, please:
- Open an issue on GitHub
- Visit the project repository
- Contact the developers

---

**Last Updated**: 2026
**Version**: 1.1 (Updated)
