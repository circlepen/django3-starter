# Pull the base image
FROM python:3.8

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN mkdir /code
RUN mkdir /code/my_project
WORKDIR /code/my_project
#Upgrade pip
RUN pip install pip -U
RUN pip install --upgrade setuptools
RUN apt-get update
RUN apt-get install python3 default-libmysqlclient-dev gcc cron vim gettext -y
RUN pip install mysqlclient uwsgi
ADD . /code/my_project
#Install dependencies
RUN pip install -r requirements.txt
