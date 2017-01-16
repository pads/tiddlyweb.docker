FROM tiddlyweb:latest
MAINTAINER Ben Paddock "pads@thisispads.me.uk"

RUN apt-get install -y nginx uwsgi supervisor
RUN pip install -U uwsgi

ADD https://raw.githubusercontent.com/tiddlyweb/tiddlyweb/master/wsgiapp.py $TIDDLYWEB_HOME

RUN echo "daemon off;" >> /etc/nginx/nginx.conf

COPY nginx.conf /etc/nginx/sites-available/default
COPY supervisor.conf /etc/supervisor/conf.d/

CMD supervisord -n