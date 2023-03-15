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

Install Django
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
GitHub Error: Authentication Failed from the Command Line
https://ginnyfahs.medium.com/github-error-authentication-failed-from-command-line-3a545bfd0ca8
github token
