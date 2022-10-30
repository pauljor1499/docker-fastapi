# pull official base image
FROM python:3.10.1-slim-buster

# set working directory (host machine to container (v env))
WORKDIR /usr/src/app

# set environment variables
ENV PYTHONDONWITEBYCODE 1
ENV PYTHONUNBUFFERED 1

# install system dependencies
RUN apt-get update
RUN apt-get -y install netcat gcc
RUN apt-get clean

# install python dependencies
RUN pip install --upgrade pip
COPY ./requirements.txt .
RUN pip install -r requirements.txt

# add app
COPY . .