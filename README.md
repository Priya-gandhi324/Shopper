# Shopper
E-commerce app
Demo: https://shopper25-1599003f66e0.herokuapp.com/


## Deploying the Shopper app on Heroku
1. Create an app on Heroku and in Resources Add-ons add Heroku Postgres
2. The Procfile and runtime.txt files needed have already been added to this repository.
3. The requirements.txt must be up to date.
4. Change the database config in the shopper app settings.py by using the Heroku Postgres credentials:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': '<DATABASE>',
        'USER': '<USER>',
        'PASSWORD': '<PASSWORD>',
        'HOST': '<HOST>',
        'PORT': '5432',
    }
}

# DATABASES = {
#     'default': {
#         'ENGINE': 'django.db.backends.sqlite3',
#         'NAME': BASE_DIR / 'db.sqlite3',
#     }
# }
```

Use this step-by-step guide to create an app on Heroku by Geeksforgeeks:  https://www.geeksforgeeks.org/deploying-django-app-on-heroku-with-postgres-as-backend/


## Running the app on local
1. Create a virtual environment and activate it:
```python
python -m venv venv
venv\Scripts\activate
```

2. Install all the necessary packages using requirements.txt
```python
pip install -r requirements.txt
```

3. Make migrations for the database:
```python
python manage.py makemigrations
python manage.py migrate
```

4. Run the server:
```python
python manage.py runserver
```
  
5. Use the admin panel to change the products
http://127.0.0.1:8000/admin
