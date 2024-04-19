# Django Web Hosting

Welcome to the Django Web Hosting guide! This repository provides instructions for hosting a Django website on [PythonAnywhere](https://www.pythonanywhere.com/). Follow the steps below to create an account on PythonAnywhere, clone the repository, set up a virtual environment, and configure your Django project.

## About

Create an account on [PythonAnywhere](https://www.pythonanywhere.com/), then follow this guide to host a Django website.

## Hosted on PythonAnywhere

- **Website Link**: [https://abhishekrajput.pythonanywhere.com/](https://abhishekrajput.pythonanywhere.com/)

## Table of Contents

- [Getting Started](#getting-started)
- [Project Configuration](#project-configuration)
- [WSGI Configuration](#wsgi-configuration)
- [Virtual Environment](#virtual-environment)

## Getting Started

1. **Create an Account on PythonAnywhere**: Sign up for an account on [PythonAnywhere](https://www.pythonanywhere.com/).

2. **Access Bash on PythonAnywhere**: Once you've created your account, navigate to the PythonAnywhere dashboard and launch a new Bash console to execute the following commands.

3. **Clone the Repository**:
    ```bash
    git clone https://github.com/Abhishek-2502/django_webhosting
    cd django_webhosting
    ```
4. **Create a Virtual Environment**:
    ```bash
    mkvirtualenv venv
    ```
5. **Get inside the Folder**:
   ```bash
    cd django_webhosting
    cd django_webhosting
    ```
6. **Install Django**:
    ```bash
    pip install django
    ```

## Project Configuration

In your Django project's `settings.py` file, make the following changes:

1. **Set Debug Mode**:
    ```python
    DEBUG = True
    ```

2. **Specify Allowed Hosts**:
    ```python
    ALLOWED_HOSTS = ['abhishekrajput.pythonanywhere.com']
    ```

3. **Configure Templates Directory**:
    ```python
    TEMPLATES = [
        {
            'BACKEND': 'django.template.backends.django.DjangoTemplates',
            'DIRS': ['/home/abhishekrajput/django_webhosting/django_webhosting/templates'],
            # Other template settings...
        },
    ]
    ```

## WSGI Configuration

In your Django project's WSGI configuration file (`wsgi.py`), add the following code:

```python
# +++++++++++ DJANGO +++++++++++
import os
import sys

path = '/home/abhishekrajput/django_webhosting/django_webhosting'
if path not in sys.path:
    sys.path.append(path)

os.environ['DJANGO_SETTINGS_MODULE'] = 'django_webhosting.settings'

from django.core.wsgi import get_wsgi_application
application = get_wsgi_application()
```

## Virtual Environment

In your PythonAnywhere account, navigate to the virtual environment section and add the virtual environment you created:

- **Add Virtual Environment**: `venv`

By following these steps, you will have successfully hosted your Django website on PythonAnywhere.

For any further assistance or issues, please feel free to open an issue or submit a pull request.
