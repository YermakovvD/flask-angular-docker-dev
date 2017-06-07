FROM python:2.7

RUN apt-get update -y 
RUN apt-get install nginx -y

ENV HOME=/usr/src/app/server
RUN mkdir -p $HOME
WORKDIR $HOME

RUN pip install -r requirements.txt

CMD python manage.py db init && python manage.py db migrate && python manage.py db upgrade && nginx && flask run --host=0.0.0.0
