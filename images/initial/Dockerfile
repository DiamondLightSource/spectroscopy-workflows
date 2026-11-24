FROM docker.io/library/python:3.12-bookworm
WORKDIR /app


COPY requirements.txt /app/requirements.txt

RUN pip install -r requirements.txt

COPY . /app/