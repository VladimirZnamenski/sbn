Create a Virtual Environment
https://docs.python.org/3/library/venv.html

Commands
Create a virtual environment:
python -m venv ./venv
Activate the virtual environment:
source ./venv/bin/activate
To see what'is installed:
pip3 freeze
To exit (deactivate) the virtual environment:
deactivate

Install Django (Django for beginners https://djangoforbeginners.com/pages-app/)
(activate the venv to install Django in the virtual environment and not globally)
pip install django

Create a gitignore file
To generate the file use https://www.gitignore.io or https://www.toptal.com/developers/gitignore
Type Django in the form on the site and click "Create". The file will be generated.
Create the ".gitignore" file in the root of the project folder
Add to the file the lines below to exclude the "venv" folder as well
### Virtual Environment ###
venv

Start a project named "sbn" (Saint-Benoit-de-Nursie) in a current "." directory
django-admin startproject sbn .

Configure git
git config user.email "zvg@mcn.com"
git config user.name "zvg"

git remote add origin https://github.com/VladimirZnamenski/sbn.git
git push --set-upstream sbn master

git add .
git commit -m ""
git push origin main

GitHub Error: Authentication Failed from the Command Line
https://ginnyfahs.medium.com/github-error-authentication-failed-from-command-line-3a545bfd0ca8
github token

Configure a Web Apprication
https://help.pythonanywhere.com/pages/DeployExistingDjangoProject/
Click Web
Modify the Code section
Source code: /home/saintbenoitdenursie/sbn/sbn (where settings.py is located)
Working directory: /home/saintbenoitdenursie/sbn
Modify /var/www/saintbenoitdenursie_pythonanywhere_com_wsgi.py
Removing everything except for DJANGO
Uncomment the DJANGO portion
Modify: path = '/home/saintbenoitdenursie/sbn'
Modify: os.environ['DJANGO_SETTINGS_MODULE'] = 'sbn.settings'

Create a static folder for static files /home/saintbenoitdenursie/sbn/static
Configure Static files: /home/saintbenoitdenursie/sbn/static

Modify ALLOWED_HOSTS = ['saintbenoitdenursie.pythonanywhere.com'] in /home/saintbenoitdenursie/sbn/sbn/settings.py

Create the Pages App
python manage.py startapp pages
add a new app to "settings.py" in the INSTALLED_APPS section "pages.apps.PagesConfig",
create /home/saintbenoitdenursie/sbn/pages/urls.py




