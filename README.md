# django-tutorial


## writing my first Django app about polls

### 1. django install

* Check out Django's main development branch:

```
$ git clone git://github.com/django/django.git
``` 

* pip install

```
$ pip install -e django/
```

More details please visit site: [How to install Django](https://docs.djangoproject.com/en/1.10/topics/install/#installing-development-version)

### 2. Create a project

**Create a project**

```
$ django-admin startproject mysite
```

**The structure of mysite is like this:**

```
mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        wsgi.py
```
**The development server**

Change into the outer mysite directory and run the following commands:

```
$ python manage.py runserver
```

You'll see the following output on the command line:

```
Performing system checks...

System check identified no issues (0 silenced).

You have unapplied migrations; your app may not work properly until they are applied.
Run 'python manage.py migrate' to apply them.

November 05, 2016 - 15:50:53
Django version 1.10, using settings 'mysite.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```

### 3. Create the Polls app

**To create your app, make sure you're in the same directory as manage.py and type this command**

```
$ python manage.py startapp polls
```

**That'll create a directory polls, which is laid out like this:**

```
polls/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py
```
This directory structure will house the poll application.

### 4. Write the Polls app

Change the urls.py, settings.py and so on.

* The outer **mysite/** root directory is just a container for your project. its name doesn't matter to Django; you can rename it to anything you like.

* **manage.py:** A command-line utility

* The inner **mysite/** directory is actual Python package for your project. 

* **mysite/settings.py** Setting/configuration for this Django project.

* **mysite/urls.py** The URL declarations for this Django project

* **mysite/wsgi.py** An entry-point for WSGI-compitable web servers to serve your projct.

* **polls/admin.py** Setting for admin and you can register your models here.

* **polls/apps.py** Configuration for the app Polls. such as the app name.

* **polls/models** Create your models here and map them to database.

* **polls/tests.py** Write automated test files.

* **polls/views.py** Write your view here. According to the mysite/urls.py, different url will call the corresponding view function. The function will return the corresponding template to users.

* **polls/urls.py** You can write urls for this app and add the urls to mysite/urls.py. Because you can write different urls for different app.

* **polls/migrations/** You have unapplied migrations; your app may not work properly until they are applied. Run 'python manage.py migrate' to apply them. If you type the command 'python manage.py runserver' directly. After the migration, it will generate the map between models and database columns.

More details please visit the site: [Writing your first Django app](https://docs.djangoproject.com/en/1.10/intro/tutorial01/)
