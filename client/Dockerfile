FROM node:6.10.3

ENV HOME=/usr/src/app
RUN mkdir $HOME
WORKDIR $HOME

RUN npm install -g  --unsafe-perm angular-cli

CMD cd ./client && npm install && ng serve --host 0.0.0.0
