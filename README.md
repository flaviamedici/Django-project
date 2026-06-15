```
pip install django
django-admin startproject mysite .
python manage.py startapp job_application
python manage.py runserver   
```

Add job_application inside INSTALLED_APPS in settings.py
```
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


create migrations: Forms class translated into python code
```
python manage.py makemigration
```
