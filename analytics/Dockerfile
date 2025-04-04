FROM python:3.10

WORKDIR /app
COPY analytics/requirements.txt /app/requirements.txt

RUN apt update -y
RUN apt install build-essential libpq-dev -y
RUN pip install --upgrade pip setuptools wheel

RUN pip install -r requirements.txt

COPY analytics/app.py /app/app.py
COPY analytics/config.py /app/config.py

EXPOSE 5153

CMD ["python3", "app.py"]