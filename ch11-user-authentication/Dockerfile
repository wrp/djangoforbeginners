

FROM python:3.11-slim


COPY accounts/ /var/www/chicory-auth
COPY django_project/ /var/www/chicory-auth
COPY manage.py  /var/www/chicory-auth
COPY templates/ /var/www/chicory-auth
COPY requirements.txt /var/www/chicory-auth
COPY fly.toml /var/www/chicory-auth


RUN (cd /var/www/chicory-auth; pip install /var/www/chicory-auth  /var/www/chicory-auth/requirements.txt)
RUN python /var/www/chicory-auth/manage.py migrate
RUN python /var/www/chicory-auth/manage.py collectstatic
