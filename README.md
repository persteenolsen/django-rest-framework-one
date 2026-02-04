# REST framework tutorial

Uses Django 5.2 and Django REST Framework 3.16

Last updated:

04-02-2026

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

## Make changes to the Database

- (.venv) python manage.py makemigrations snippets

- (.venv) python manage.py migrate

## Create a Super User Account 

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

Happy use of Django with REST Framework :-)




