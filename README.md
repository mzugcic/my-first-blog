# My blog

This is a web application written in Django made with some help of the tutorial's at [DjangoGirls](http://tutorial.djangogirls.org/en/django/). The blog is deployed to Heroku and PythonAnywhere. The blog allows the user (me) to add posts, edit and remove draft post, or publish them. Visitors can comment the posts, but the admin has the possibility to remove or approve the comments, furthemore there is a comment counter which counts the number of approved comments. The blog also shows the creation date and time of every post and comment.

----
## Dependencies
Programs and applications used:

* Python
* Django 1.9
* PostgreSQL
* Gunicorn
* Whitenoise
* Psycopg

Accounts used:

* [GitHub](https://github.com/)
* [PythonAnywhere](https://www.pythonanywhere.com/)
* [Heroku](https://www.heroku.com/)

----
## Installation
The blog was made in Windows and some of the programs have to bedownloaded from their host websites and then installed: 

* [Python](https://www.python.org/downloads/release/python-343/)
* [Atom](https://atom.io/) - code editor
* [Git](https://git-scm.com/)

and some can be installed using the command line:

* Django - was installed in the virtual environment:

    `pip install django~=1.9.0`

## Project

Django is used through the command line and within Django you have to create directories and files:

    (myvenv)  django-admin startproject mysite .


`(myvenv)` - stands for *virtual environment* and you can learn more about it [here](https://virtualenv.pypa.io/en/latest/).

For the database you will first use the default one `sqlite3` and to create it run:

    python manage.py migrate
    
After that it is necesary to start the web server:

    python manage.py runserver
    
And then in a browser enter the adress (to see if it is working):

    http://127.0.0.1:8000/


##Deployment
Deploying from the computer to the website was done by using *GitHub* and the server providers *PythonAnywhere* and *Heroku*.


###PythonAnywhere

This was the first server provider I used. Deploying to *PythonAnywhere* is done in the *Bash* console on the *PythonAnywhere* site and you should always use a virtualenv when deploying. You can pull the code to *PythonAnywhere* by using the next command:

    (myvenv)$ git pull
When the code is downloaded it can be viewed in the *Files* tab. To upload the web site you have to go to the *Web* tab and hit *Reload*. There is a link above the *Reload* button that then takes you to the updated app, in my example:

[https://mzugcic.pythonanywhere.com](https://mzugcic.pythonanywhere.com).

###Heroku
*Heroku* uses *Postgres* for the database while you would, like I did, use the default *SQLite* on your computer. Some of the files have to be modified so they could run on *Heroku*. 

Deploying to *Heroku* can be done directly through the command line on the computer using the command:

    git push heroku master

When the code is deployed you have to start the web process by runing the command:
    
    heroku ps:scale web=1

To visit the blog in the browser run: 

    heroku open

My app can be visited here:

[https://zugatestblog.herokuapp.com/](https://zugatestblog.herokuapp.com/).


##Aditional features
In the making of the blog I used HTML files for templates and CSS files for visual editing, and both were supported with *Bootstrap* - the framework for developing websites.

For the customization of the fonts and colors of the text in the app I used fonts from [Google Fonts](https://www.google.com/fonts) and colors from [Color Picker](http://www.colorpicker.com/).

I also used *Django ORM* which allows reading data from the database, filtering it and ordering it.

##External links
* [Django Girls](http://tutorial.djangogirls.org/) tutorials
* [Stack Overflow](http://stackoverflow.com/), [GitHub Help](https://help.github.com/) error documentanion and help 
