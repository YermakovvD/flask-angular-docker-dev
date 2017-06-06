FROM python:2.7

RUN apt-get update -y 
RUN apt-get install nginx -y

ENV HOME=/usr/src/app
RUN mkdir $HOME
WORKDIR $HOME

CMD pip install -r ./server/requirements.txt && nginx && flask run --host=0.0.0.0
