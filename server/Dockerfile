FROM python:2.7

RUN apt-get update -y 
RUN apt-get install nginx -y

ENV HOME=/usr/src/app/server
RUN mkdir -p $HOME
WORKDIR $HOME

RUN rm /bin/sh && ln -s /bin/bash /bin/sh

CMD /usr/src/app/server/venv/bin/pip install -r requirements.txt && /usr/src/app/server/venv/bin/python manage.py db init && /usr/src/app/server/venv/bin/python manage.py db migrate && /usr/src/app/server/venv/bin/python manage.py db upgrade && nginx && /usr/src/app/server/venv/bin/flask run --host=0.0.0.0
