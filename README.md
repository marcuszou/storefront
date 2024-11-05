# alfonShop - storeFront

## Tech Stack

1. Python3: 3.11.10 (macOS Sonoma and Ubuntu 24.04)
2. Django: 5.1.2

Ubuntu 22.04 bears Python 3.10.12, and it's okay to use Python 3.10 to run this project.
In case of someones wanting to have Python 3.11 in Ubuntu 22.04, here is the How-to:

```shell
sudo apt update -y
sudo apt install -y software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update -y
sudo apt install python3.11
```
## Setup

It's way better to setup a Virtual Env for any Python project, here is the how-to:
```shell
## Install virtualenv tool
sudo apt install python3-virtualenv
## in MacOS
## sudo port install python3-virtualenv
## Create a virtual env with name of ".venv" in Python3.11
mkdir myStore
cd myStore
virtualenv .venv
## In case of host having Python 3.10 (Ubuntu 22.04) but you perfer Python 3.11 in the venv
virtualenv -p python3.11 .venv
## In case of you are a fan of the Python3 module (venv)
## python3 -m venv .venv

# activate the .venv
source .venv/bin/activate
## in Windows, be like: 
## .venv\bin\activate.bat

# Install django
pip install -r requirements.txt

## Create and run the Django project in current folder
django-admin startproject storeFront .
## Add an app - playground
python manage.py startapp playground
## append the 'playground', to the INSTALLED_APPS Section of storeFront project folder

```

## Daily Coding under .venv please

```
cd storeFront
code .
source .venv/bin/activate
```

## Coding

### Django Supported Database Engines
- SQLite  (Intro to this)
- PostgreSQL
- MySQL   (then focus on this)
- MariaDB
- Oracle
- MS SQL Server
### 4.3 Migration of SQLite
```shell
python manage.py makemigrations
```
<<<<<<< HEAD
### 4.4 migrate
```shell
python manage.py migrate
```
Also install a VScode extension: SQLite (by alexcvzz)
=======
### 4.6 reverting migrations
```shell
python manage.py migrate store 003 ## the last step was 004
```
Then delete related files, that's very tideous!
The best way is to use git
```shell
git log --oneline
git reset --hard HEAD~1
```
>>>>>>> a844af3 (update 4.8)

## License
MIT
