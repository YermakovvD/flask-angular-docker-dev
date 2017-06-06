FROM python:2.7

ENV HOME=/usr/src/app
RUN mkdir $HOME
WORKDIR $HOME

CMD pip install -r ./server/requirements.txt && flask run --host=0.0.0.0
