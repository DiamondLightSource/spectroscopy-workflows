FROM docker.io/library/python:3.12-bookworm as builder

COPY requirements.txt .

RUN pip install -r requirements.txt

FROM debian:bookworm

COPY --from=builder . .
