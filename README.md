# 🎓 Cultural Relations Directorate Management System

[![Django](https://img.shields.io/badge/Django-4.1.3-green.svg)](https://www.djangoproject.com/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.2.0-purple.svg)](https://getbootstrap.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A comprehensive web-based application designed to automate and streamline the operations of the Cultural Relations Directorate at the University. This system manages demonstrators (teaching assistants), their dispatches, graduate studies, and related administrative processes.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Key Modules](#key-modules)
- [Database Schema](#database-schema)
- [Security Features](#security-features)
- [Contributing](#contributing)
- [Team](#team)
- [License](#license)

## 🎯 Overview

**Project Duration:** September 2022 - August 2023

This Django-based management system provides a complete solution for tracking and managing teaching assistants throughout their academic journey, from initial nomination through various dispatches and graduate studies.

### Key Highlights

- ✅ Developed Django backend with full CRUD operations
- ✅ Created SQL scripts for data management and optimization
- ✅ Built responsive front-end with JavaScript, HTML5, and CSS3
- ✅ Implemented advanced search filters with query builder
- ✅ Automated email notifications via Gmail API and SMTP
- ✅ Designed dynamic reports and statistical diagrams
- ✅ Full RTL (Right-to-Left) support for Arabic language

## ✨ Features

### 📊 Data Management

- **Demonstrator Management**
  - Personal information tracking
  - University degree records
  - Graduate studies (Diploma, Master's, PhD)
  - Excellence certificates
  - Status tracking (demonstrator, returning, envoy, etc.)

- **Dispatch Management**
  - Internal and external dispatch tracking
  - Extension and freeze period management
  - Duration calculations and remaining time
  - Progress reports and supervisor information

### 🔍 Advanced Search & Filtering

- Complex query builder with AND/OR conditions
- Multiple filter criteria
- Export results in CSV/Excel formats
- Save and reuse query templates

### 📧 Automated Notifications

- Extension notifications to demonstrators
- Late dispatch warnings
- Bulk communications to colleges
- Unsent extension reminders

### 📈 Reporting & Analytics

- Statistical dashboards with Chart.js
- Interactive data tables with Tabulator.js
- Visual data representations
- Excel/CSV export with Arabic support

### 👥 User Management

- Role-based access control
- Department-based permissions
- Staff account management
- Secure authentication system

## 🛠️ Technology Stack

### Backend
```
Django 4.1.3
Django REST Framework
SQLite3
Python 3.8+
```

### Frontend
```
JavaScript (ES6+)
HTML5
CSS3
Bootstrap 5.2.0 (RTL)
jQuery
```

### Libraries & Tools
```
Chart.js - Data visualization
Tabulator.js - Advanced tables
jQuery QueryBuilder - Complex searches
Toastify - Notifications
Font Awesome 6.2.1 - Icons
Papaparse - CSV processing
SheetJS - Excel processing
```

## 🚀 Installation

### Prerequisites

```bash
Python 3.8 or higher
pip (Python package manager)
Git
```

### Step-by-Step Installation

1. **Clone the repository**
```bash
git clone https://github.com/manzalji-abed/Cultural-Relations-Directorate-Automation.git
cd cultural-relations-system
```

2. **Create and activate virtual environment**
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

If `requirements.txt` doesn't exist, install manually:
```bash
pip install django==4.1.3
pip install djangorestframework
```

4. **Apply database migrations**
```bash
python manage.py migrate
```

5. **Create superuser account**
```bash
python manage.py createsuperuser
```

6. **Collect static files**
```bash
python manage.py collectstatic
```

7. **Run development server**
```bash
python manage.py runserver
```

8. **Access the application**
```
http://localhost:8000
```

### Environment Variables

Create a `.env` file in the project root:

```env
SECRET_KEY=your-secret-key-here
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1

# Email Configuration
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USE_TLS=True
EMAIL_HOST_USER=your-email@gmail.com
EMAIL_HOST_PASSWORD=your-app-password
```

## 💻 Usage

### Login

1. Navigate to `http://localhost:8000/app/login`
2. Enter your credentials (use superuser account created during installation)
3. Access the main dashboard

### Main Features

#### 1. Demonstrator Registration
- Navigate to Register Demonstrator
- Fill in personal information, contact details, and academic qualifications
- Submit the form to create a new demonstrator profile

#### 2. Dispatch Management
- Select a demonstrator from Demonstrators
- Click on Add New Dispatch
- Enter dispatch details including country, university, and duration
- System automatically calculates end dates and remaining time

#### 3. Advanced Search
- Go to Query
- Use the visual query builder to create complex searches
- Select fields to display in results
- Export results to Excel or CSV

#### 4. Email Notifications
- Navigate to Send Email
- Choose recipients (individual, college, or bulk)
- Compose message and send
- System tracks sent emails and pending notifications

#### 5. Reports & Statistics
- View dashboard for overview statistics
- Generate custom reports based on filters
- Export data for external analysis
- View visual charts and graphs

## 🔑 Key Modules

### 1. Demonstrator Management Module
Handles complete lifecycle of demonstrator records including:
- Personal and contact information
- Academic qualifications
- Employment status
- Graduate studies tracking

### 2. Dispatch System Module
Manages all aspects of dispatches:
- Dispatch decisions and approvals
- Extension and freeze periods
- Duration calculations
- Supervisor information
- Progress reports

### 3. Query Builder Module
Advanced search functionality:
- Visual query construction
- Complex AND/OR conditions
- Multiple data types (string, date, select)
- Result customization and export

### 4. Email Notification Module
Automated communication system:
- Template-based emails
- Scheduled notifications
- Bulk sending capabilities
- Delivery tracking

### 5. Reporting Module
Data analysis and visualization:
- Statistical dashboards
- Custom report generation
- Data export in multiple formats
- Visual charts and graphs

## 📊 Database Schema

### Core Models

**Demonstrator**
- Personal information
- Contact details
- Academic qualifications
- Current status

**Dispatch**
- Dispatch details and decisions
- Duration management
- Supervisor information
- Related extensions and freezes

**Extension**
- Extension decisions
- Duration modifications
- Email tracking

**Freeze**
- Freeze decisions
- Duration specifications
- Reason tracking

**GraduateStudies**
- Degree type (Diploma/Master's/PhD)
- University and department
- Graduation year and average

**Permissions**
- Department definitions
- User access rights

## 🔒 Security Features

- **Authentication**
  - Django's built-in authentication system
  - Password validation and encryption
  - Session management

- **Authorization**
  - Role-based access control
  - Department-based permissions
  - Superuser privileges

- **Data Protection**
  - CSRF protection
  - SQL injection prevention
  - XSS protection
  - Secure password storage

- **Middleware**
  - Custom user checking
  - Session validation
  - Request filtering

## 👥 User Roles

### Super Administrator
- Full system access
- User management
- Department configuration
- Data import/export
- System settings

### Department Staff
- Demonstrator management
- Dispatch operations
- Report generation
- Email communications
- Limited to assigned departments

## 📝 API Endpoints

The system includes REST API endpoints for:

```
GET    /app/allDemonstrators/          - List all demonstrators
GET    /app/demonstrator/<id>/         - Demonstrator details
POST   /app/insert/                    - Create demonstrator
PUT    /app/updateDemon/<id>/          - Update demonstrator
DELETE /app/deleteDemon/<id>/          - Delete demonstrator

POST   /app/dispatch/<id>/             - Create dispatch
PUT    /app/updateDispatch/<id>/       - Update dispatch
DELETE /app/deleteDispatch/<id>/       - Delete dispatch

POST   /app/query/                     - Execute custom query
GET    /app/download/                  - Export data
POST   /app/sendEmails/                - Send emails
```

## 🎨 UI Features

- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **RTL Support**: Full right-to-left layout for Arabic
- **Dark/Light Themes**: Customizable color schemes
- **Interactive Tables**: Sortable, filterable data tables
- **Modal Dialogs**: Clean popup interfaces for actions
- **Toast Notifications**: Real-time feedback messages
- **Form Validation**: Client and server-side validation
- **Date Pickers**: Arabic-localized date selection

## 🔧 Configuration

### Django Settings

Key settings in `projectFifthYear/settings.py`:

```python
# Language and timezone
LANGUAGE_CODE = 'ar-us'
TIME_ZONE = 'UTC'
USE_I18N = True
USE_TZ = True

# Static files
STATIC_URL = 'static/'
STATICFILES_DIRS = (BASE_DIR / 'static',)

# Database
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}
```

### Email Configuration

Configure email settings for notifications:

```python
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp.gmail.com'
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = 'your-email@example.com'
EMAIL_HOST_PASSWORD = 'your-password'
```

## 🐛 Troubleshooting

### Common Issues

**Issue: Database locked error**
```bash
# Solution: Close all connections and restart server
python manage.py migrate --run-syncdb
```

**Issue: Static files not loading**
```bash
# Solution: Collect static files again
python manage.py collectstatic --clear
```

**Issue: Email not sending**
```bash
# Check email configuration in settings.py
# Ensure Gmail app password is correct
# Verify firewall/antivirus not blocking SMTP
```

## 📚 Documentation

For detailed documentation on specific features:

- [User Guide](docs/USER_GUIDE.md) - End-user documentation
- [Admin Guide](docs/ADMIN_GUIDE.md) - Administrative functions
- [API Documentation](docs/API.md) - REST API reference
- [Developer Guide](docs/DEVELOPER.md) - Technical documentation

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Coding Standards

- Follow PEP 8 for Python code
- Use meaningful variable and function names
- Add comments for complex logic
- Write docstrings for functions and classes
- Test thoroughly before submitting PR


