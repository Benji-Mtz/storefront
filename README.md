## Ultimate Django Series

First we will install *`pipenv`*

```sh
pip3 install pipenv

mkdir storefront
cd storefront
pipenv install django # Pipfile, Pipfile.lock

pipenv shell # activate env, exit (similar to deactivate) for quit

(env) django-admin startproject storefront .
(env) python manage.py runserver
(env) pipenv --venv # + /bin/python for interprete IDE
(env) python manage.py startapp playground
(env) pipenv install django-debug-toolbar
```

add the this apps on apps section of the file `./storefront/settings.py`
```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'playground',
    'debug_toolbar'
]
```