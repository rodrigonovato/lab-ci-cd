FROM python:3.10.20-alpine3.24
LABEL MANTAINER="Rodrigo Novato"

WORKDIR /app

COPY . /app

RUN apk add --no-cache curl \
    && pip install --trusted-host pypi.python.org -r requirements.txt

EXPOSE 8000

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "app:app"]