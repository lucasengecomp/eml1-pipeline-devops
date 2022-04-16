FROM python:3.10.2-slim

WORKDIR /usr/src/app

COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

ENTRYPOINT ["gunicorn", "-w", "4", "-b", "127.0.0.1:5000", "app:app"]