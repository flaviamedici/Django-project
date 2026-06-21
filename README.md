````markdown
# 📝 Django Job Application Form

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Django](https://img.shields.io/badge/Django-Framework-green?logo=django)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5-purple?logo=bootstrap)
![SQLite](https://img.shields.io/badge/Database-SQLite-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)

A web-based job application system built with **Django**, **Bootstrap**, and **SQLite**. Applicants can submit their personal information, availability date, and employment status through a responsive form. Submitted applications are stored in a database and a confirmation email is sent to the applicant.

---

## 📌 Features

- Collect applicant information through a web form
- Store submissions in a SQLite database using Django Models
- Send confirmation emails after successful submission
- Display success messages to users
- Responsive Bootstrap UI
- Django ORM integration
- Form validation using Django Forms
- Easy-to-extend project structure

---

## 🛠 Technologies Used

- Python
- Django
- SQLite
- Bootstrap 5
- HTML5
- Django Messages Framework
- Django Email Backend

---

## 📂 Project Structure

```text
job_application/
│
├── models.py
├── views.py
├── forms.py
├── templates/
│   └── index.html
│
mysite/
│
├── settings.py
├── urls.py
│
manage.py
```

---

## 🗄 Database Model

The application stores job applications using the following Django model:

```python
class Form(models.Model):
    first_name = models.CharField(max_length=80)
    last_name = models.CharField(max_length=80)
    email = models.EmailField()
    date = models.DateField()
    occupation = models.CharField(max_length=80)
```

### Stored Information

| Field | Description |
|---------|------------|
| First Name | Applicant's first name |
| Last Name | Applicant's last name |
| Email | Applicant's email address |
| Date | Available start date |
| Occupation | Current employment status |

---

## 🖥 User Interface

The application provides a simple Bootstrap-powered form where users can:

- Enter first and last name
- Provide an email address
- Select an available start date
- Choose employment status:
  - Employed
  - Unemployed
  - Self-Employed
  - Student

After submission:

✅ Data is saved to the database

✅ A confirmation email is sent

✅ A success message is displayed

---

## ⚙️ Installation

### 1. Install Django

```bash
pip install django
```

---

### 2. Create a Django Project

```bash
django-admin startproject mysite .
```

---

### 3. Create the Application

```bash
python manage.py startapp job_application
```

---

### 4. Register the App

Add the application inside `INSTALLED_APPS` in `settings.py`:

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'job_application',
]
```

---

### 5. Create Database Migrations

Django translates the model classes into database tables using migrations.

Generate migration files:

```bash
python manage.py makemigrations
```

Apply migrations:

```bash
python manage.py migrate
```

---

### 6. Run the Development Server

```bash
python manage.py runserver
```

Open:

```text
http://127.0.0.1:8000/
```

---

## 📧 Email Notifications

After a successful submission, Django sends a confirmation email to the applicant.

Example:

```text
Subject: Form Submission Confirmation

A new job application was submitted.
Thank you, John.
```

To enable email functionality, configure your email settings in `settings.py`.

Example:

```python
EMAIL_HOST = "smtp.gmail.com"
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = "your_email@gmail.com"
EMAIL_HOST_PASSWORD = "your_password"
```

---

## 🔄 Application Workflow

```text
User Opens Form
        │
        ▼
Completes Application
        │
        ▼
Form Validation
        │
        ▼
Save to SQLite Database
        │
        ▼
Send Confirmation Email
        │
        ▼
Display Success Message
```

---

## 🚀 Future Improvements

- Admin dashboard for reviewing applications
- Resume/CV upload support
- Email templates with HTML formatting
- Applicant tracking system
- Search and filtering functionality
- PostgreSQL integration
- User authentication for recruiters

---

## 📚 What I Learned

This project demonstrates:

- Django project structure
- Django Models and ORM
- Form handling and validation
- Database migrations
- Sending emails with Django
- Bootstrap integration
- Template rendering
- Django Messages Framework

---

## 📄 License

This project is open-source and available under the MIT License.

---

### 👨‍💻 Author

Built as a Django learning project to practice:

- Web development
- Database integration
- Form processing
- Email automation
- Django best practices
````
