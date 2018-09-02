FROM python:3.6

RUN apt-get update -y 
RUN apt-get install nginx -y

ENV HOME=/usr/src/app/server
RUN mkdir -p $HOME
WORKDIR $HOME

COPY requirements.txt /tmp
WORKDIR /tmp
RUN pip install -r requirements.txt

CMD nginx && flask run --host=0.0.0.0
