FROM python:3.7
VOLUME /app
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
RUN pip install uwsgi
COPY . .
CMD uwsgi \
    --wsgi-file vesta/wsgi.py \
    --http :8000
