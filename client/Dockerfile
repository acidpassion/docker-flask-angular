FROM node:8.9.0

ENV HOME=/usr/src/app
RUN mkdir $HOME
WORKDIR $HOME

RUN npm install -g @angular/cli

# CMD cd ./client && npm rebuild node-sass --force && npm install && ng serve --host 0.0.0.0

CMD cd ./client && npm install && ng serve --host 0.0.0.0