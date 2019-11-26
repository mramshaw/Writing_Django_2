# Writing Django 2

Having investigated [Django 1 with Python 2](http://github.com/mramshaw/Writing_Django) it seemed
time to investigate Django __2__ with Python __3__, mainly because Python 2 support ends in 2020.

[As my initial exercise was pretty straightforward, rather than try to update that repo, I will
 simply recreate the whole exercise with Django 2 and Python 3. For more details, please refer to
 the original repo.]

# Django LTS

Note that we will use the __LTS__ version of Django 2, which at the time of writing (November 2019)
is __2.2.7__.

This release requires Python [3.5 or more recent](http://docs.djangoproject.com/en/2.2/faq/install/#faq-python-version-support).

# Python 3

Verify the version of Python as follows:

```bash
$ python3 --version
Python 3.5.2
$
```

[I have both Python 2 and Python 3 installed. On my system, Python 2 is `python`
 while Python 3 is `python3`. Likewise Python 2 uses `pip` while Python 3 uses
 `pip3`. In the instructions that follows I will use `python3` and `pip3` but
 these may be replaced with `python` and `pip` for sytems where only Python 3
 is installed.]

# Prerequisites

Install the latest version of Django (plus dependencies) as follows:

    $ pip3 install --user -r requirements.txt

Verify the installed version of Django as follows:

    $ python3 -m django --version

This should look as follows:

```bash
$ python3 -m django --version
2.2.7
$
```

## Create a Project

Use the `django-admin` command to do this:

    $ django-admin startproject polls

And time to see if everything works so far:

    $ cd polls
    $ python3 manage.py runserver

The results should be something like:

```bash
$ python3 manage.py runserver
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 17 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.

November 26, 2019 - 16:48:54
Django version 2.2.7, using settings 'polls.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
[26/Nov/2019 16:49:27] "GET / HTTP/1.1" 200 16348
[26/Nov/2019 16:49:28] "GET /static/admin/css/fonts.css HTTP/1.1" 200 423
[26/Nov/2019 16:49:28] "GET /static/admin/fonts/Roboto-Bold-webfont.woff HTTP/1.1" 200 86184
[26/Nov/2019 16:49:28] "GET /static/admin/fonts/Roboto-Regular-webfont.woff HTTP/1.1" 200 85876
[26/Nov/2019 16:49:28] "GET /static/admin/fonts/Roboto-Light-webfont.woff HTTP/1.1" 200 85692
Not Found: /favicon.ico
[26/Nov/2019 16:49:28] "GET /favicon.ico HTTP/1.1" 404 1971
^C$
```

The development server at http://127.0.0.1:8000/ should look something like:

![Development_Server](images/Development_Server.png)

# Create an App

This needs to be done in the folder where `manage.py` lives:

    $ python3 manage.py startapp polls_app

# Versions

* Django __2.2.7__
* gunicorn __20.0.2__
* Python __3.5.2__

# To Do

- [ ] Follow parts 3 - 7 of this tutorial

# Credits

Part 1:

    http://docs.djangoproject.com/en/2.2/intro/tutorial01/

Part 2:

    http://docs.djangoproject.com/en/2.2/intro/tutorial02/
