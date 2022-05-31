FROM python:3.10-buster

COPY ./requirements/backend.in /app/requirements/backend.in
WORKDIR /app

RUN python3 -m venv ./.venv
RUN . ./.venv/bin/activate
RUN pip install -r requirements/backend.in

COPY ./build/index.html /app/build/index.html
COPY ./spaceship /app/spaceship

CMD ["uvicorn", "spaceship.main:app", "--host=0.0.0.0", "--port=8080"] 