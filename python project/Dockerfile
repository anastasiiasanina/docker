FROM python:3.10-alpine

COPY ./requirements/backend.in /app/requirements/backend.in
WORKDIR /app

RUN apk add build-base
RUN python3 -m venv ./.venv
RUN . ./.venv/bin/activate
RUN pip install -r requirements/backend.in

COPY ./spaceship /app/spaceship
COPY ./builder/index.html /app/builder/index.html

CMD ["uvicorn", "spaceship.main:app", "--host=0.0.0.0", "--port=8080"] 