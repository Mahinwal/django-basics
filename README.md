# Django setup in virtual enviourment (CENTOS7) and PyMysql
1. Install Python3
2. Install pip3
3. Install virtualenv Ex: pip3 install virtualenv
``` pip3 install virtualenv ```
4. mkdir djangobasics 
5. cd djangobasics
6. create virtualenv here
``` sudo virtualenv venv -p python3```
7. Activate virtualenv 
```source venv/bin/activate```
8. Install PyMysql 
``` sudo pip3 install PyMySQL ```
9.Install Django 
``` sudo pip3 install django ```
10. Create Djano project
``` django-admin startproject djangobasics ```
11. Edit manage.py file and add:
``` 
import pymysql
pymysql.version_info = (1, 4, 2, "final", 0)
pymysql.install_as_MySQLdb()
```
12. Edit settings.py file for database configuration and this code in it. 
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql', 
        'NAME': 'djangobasics',
        'USER': 'root',
        'PASSWORD': 'root',
        'HOST': 'localhost',   # Or an IP Address that your DB is hosted on
        'PORT': '3306',
    }
}
```
13. Runserver with this command
``` python manage.py runserver ```

It's done!

Enjoy :) 
