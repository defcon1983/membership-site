# membership-site

A framework for launching new Django membership site quickly on to an Ubuntu 18.04 LTS instance on [Amazon Lightsail](https://aws.amazon.com/lightsail/). Comes with an complete user authentication flow, custom user model, environment variables, and social authentication options via Gmail, Facebook, Twitter, etc. This project is heavily inspired by [DjangoX](https://github.com/wsvincent/djangox)

## Features

- Django 2.1 and Python 3.7
- PostgreSQL database
- Dockerized containers
- NGINX and Gunicorn for production

## Setup:

### local:

Use pipenv
- `cd membership-site && pipenv install`

### production:

steps to deploy to production:
- `cd membership-site && sudo chmod u+x ubuntu-start.sh`
- `echo -e "yes\nyes\nyes" | ./ubuntu-start.sh`
- log out & back in
- `docker-compose up --build -d`

migrate & collectstatic
- `sudo chmod u+x site/deploy-tasks.sh`
- `./site/deploy-tasks.sh`
