# Python + Django REST Framework + PostgreSQL + Models + Vercel

This example shows how to use Django 5 on Vercel with Serverless Functions using the [Python Runtime](https://vercel.com/docs/concepts/functions/serverless-functions/runtimes/python).

Last updated 17-02-2026

Node version selected at Vercel Cloud: 22

## Demo at Vercel

https://django-rest-framework-one.vercel.app

## Installing

- Download Python from the official website [Python](https://python.org/)
- Make sure that you have installed Python by the command in Powershell: "python --version"
- Download the Python extension for Visual Studio Code which automatically include the Pylance extionsion
- Download / fork this Django Starter Website from my GitHub
- Create the virtual envirement ".venv" for the Django Web App by Powershell or by VS Code
- Virtual Enviroment by VS Code: "View - Command Palette - Python Create Enviroment"

## Install by Python commands in Powershell at Windows 10

- python -m venv .venv

- cd .venv

- Copy requirements.txt to .venv

- Scripts/activate

- (.venv) pip install -r requirements.txt

- (.venv) pip freeze > requirements.txt

- (.venv) cd ../

- (.venv) python manage.py runserver

## Start the Django Application locally

- cd .venv

- Scripts/activate

- (.venv) cd ../

- (.venv) python manage.py runserver

## Make changes to the PostgreSQL Database

- (.venv) python manage.py makemigrations snippets

- (.venv) python manage.py migrate

## Create a Super User Account for the Django Admin and REST framework

(.venv) python manage.py createsuperuser

## Test that the Django is up and running locally

- http://127.0.0.1:8000

## Open Django admin

- http://127.0.0.1:8000/admin

- Log in with your superuser account

- Click on the "+ Add" button next to Snippets. And create two new snippets

## Browsable API

Django Rest Framework ships with a browsable API that we can now use by run

- (.venv) python manage.py runserver

Navigate to the Snippets List endpoint at

- http://127.0.0.1:8000/snippets

or take a look at the the API Root

- http://127.0.0.1:8000

## Deployment to Vercel

Make sure that your static files are ready by running

```bash
python manage.py collectstatic
```
Take a look at the file `vercel.json`

Make sure to set Debug = False in the file `vercel_app/settings.py`

## Static files for Django Admin and the REST framework

There is only one Django App in the Project and the dir 'static' can be created at root level

Make sure that the Python package 'whitenoise' is installed from the requirements.txt

Note: Make sure you have the line 'whitenoise.middleware.WhiteNoiseMiddleware' in the 

MIDDLEWARE = [] at the `vercel_app/settings.py` along with the other packages

Finally, take a look at `vercel_app/settings.py`:

Find where Django now looks for the static files

STATIC_URL = 'static/'

Where you put your static files in the dir 'static'

STATIC_ROOT = BASE_DIR/'static' 

Create the static files (if not allready creaded) by the command below

```bash
python manage.py collectstatic
```
Make a commit to Github and the Django Admin + REST framework should serve static files 

Happy use of Django with REST Framework :-)




