FROM python:3.5
MAINTAINER hojin jun hojin.jun@house142.com
ENV PYTHONUNBUFFERED 1

# Setup Debian linux
RUN export DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get -y install build-essential


COPY ./backend/requirements /requirements

RUN pip install -r /requirements/local.txt

COPY ./docker/django/local/start.sh /start.sh
RUN sed -i 's/\r//' /start.sh \
    && chmod +x /start.sh

ENTRYPOINT ["/start.sh"]