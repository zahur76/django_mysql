## Steps to connect to mysql database

1. Create a new database in MySQL Workbench

    * open workbench add schema using database name

2. Create user and connect to database

    * Go to server > user and priviledges > add account
    * create user login name and password
    * go to tab schema priviledges and add database defined in step 1

4. Run ``` pip install mysqlclient ```

3. Update Django settings to connect to db

    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.mysql',
            'NAME': 'zahur', # Database name
            'USER': 'zahur', # Assigned User
            'PASSWORD': '******', # Assinged user password
            'HOST': '127.0.0.1',
            'PORT': '3306',
            'OPTIONS': {
                'init_command': "SET sql_mode='STRICT_TRANS_TABLES'"
            }
        }
    }
