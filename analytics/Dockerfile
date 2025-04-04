FROM python:3.11-slim

RUN apt update -y
RUN apt install -y build-essential libpq-dev
RUN pip install --upgrade pip setuptools wheel

WORKDIR /app

COPY analytics/requirements.txt /app/requirements.txt
RUN pip install -r requirements.txt

COPY analytics/app.py /app/app.py
COPY analytics/config.py /app/config.py

EXPOSE 5153

CMD ["python", "app.py"]