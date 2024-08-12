# A simple but fast Url Shortener
This is a simple Django project implemented to work as an efficient and high-speed URL Shortener. 
Async tasks are handled using Celery. Furthermore, in order to optimize the response time, this project uses Redis as a cache backend. Some tiny optimizations are also performed in Views.

## Table of contents

- [Requirements](#requirements)
- [Getting started](#getting-started)

## Requirements

* [Python3](https://www.python.org/)
* [Django](https://www.djangoproject.com/)
* [Django Rest Framework](https://www.django-rest-framework.org/)
* [Reddis](https://redis.io/)
* [Celery](http://www.celeryproject.org/)

## Project Overview

The project is a [Django](https://www.djangoproject.com/start/) application. It serves a URL Shortener using DRF. 

## Getting started

#### Clone the repository

```bash
git clone [https://gitlab.com/ehsanmqn/urlshortener](https://github.com/ehsanmqn/url-shortener)
```

#### Prepare the project
```bash
cd url-shortener
virtualenv -p pyhton3 venv
source venv/bin/activate
pip install -r requirements.txt
```

#### Run celery worker

```bash
--celery -A UrlShortener worker -B -l info
python -m celery -A UrlShortener worker -l info

python -m celery -A UrlShortener beat -l info
```

#### Run project

```bash
./manage.py runserver 8000
```

After running the project, it will be accessed through port 8000

#### Happy coding!


deactivate     


Remove-Item -Recurse -Force venv  

  py -3.11 -m venv venv  

env\Scripts\activate  

pip install --upgrade pip  

cd .\venv\

cd .\Scripts\ 

python.exe -m pip install --upgrade pip 

pip install -r requirements.txt    




User1: 
$env:EMAIL_USER="ghugeajinkya2701@gmail.com"
$env:EMAIL_PASS="ivgi scja ohxy pwjj"

{
  "name": "testuser",
  "email": "ghugeajinkya2701@gmail.com",
  "password": "asdfg@9876"
}
--for login refer email id as 'username'  
token : 24a6a2c1dc5693ac9a09ce498709f55712b7d1df44	



2nd user:
register request:
	{
	  "name": "testuser1",
	  "email": "testuser1@gmail.com",
	  "password": "asdfg@9876",
	  "phone": "9876543210"
	}
response: 
{
    "token": "d87b64b79b82ae606dcb271827daffbfcfcf1ba1",
    "username": "testuser1@gmail.com"
	
}


Login user:
{
  "username": "testuser1@gmail.com",
  "password": "asdfg@9876"
}
response
{
    "token": "d87b64b79b82ae606dcb271827daffbfcfcf1ba1"
}

URL shortener:
{
  "url": "https://www.overleaf.com/project/69e62a0d378318c89e9b3d0b"
}

response:
{
    "url": "http://127.0.0.1:8000/r/l5"
}


3rd user:
Register:
{
  "name": "testuser2",
  "email": "testuser2@gmail.com",
  "password": "asdfg@9876",
  "phone": "9876543211"
}
response:
{
    "token": "d4fd4d02575b89a0662f98202a4abfbcef4f35f1",
    "username": "testuser2@gmail.com"
}
Login
{
  "username": "testuser2@gmail.com",
  "password": "asdfg@9876"
}
response:
{
    "token": "d4fd4d02575b89a0662f98202a4abfbcef4f35f1"
}

{
    "url": "http://127.0.0.1:8000/r/nR"
}

working URLs for this project:
http://127.0.0.1:8000/api/v1/auth/register/
http://127.0.0.1:8000/api/v1/auth/login/
http://127.0.0.1:8000/api/v1/url/
http://127.0.0.1:8000/api/v1/url/1/analytics/7/
http://127.0.0.1:8000/r/<hash>/