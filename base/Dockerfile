FROM python:2.7-slim
MAINTAINER Ben Paddock "pads@thisispads.me.uk"

ENV TIDDLYWEB_HOME /var/tiddlyweb
RUN mkdir $TIDDLYWEB_HOME
COPY tiddlywebconfig.py $TIDDLYWEB_HOME

RUN apt-get update
RUN apt-get install -y python-pip python-dev
RUN pip install -U pip
RUN pip install -U tiddlyweb

WORKDIR $TIDDLYWEB_HOME
CMD twanager server