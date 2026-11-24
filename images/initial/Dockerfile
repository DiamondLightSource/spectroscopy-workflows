FROM docker.io/library/python:3.12-bookworm
WORKDIR /app


COPY requirements.txt /app/requirements.txt

RUN python -m venv /app/venv

RUN source /app/venv/bin/activate

RUN pip install -r requirements.txt

COPY . /app/

ENV PATH="/app/venv/$PATH"

CMD ["python", "test.py"]