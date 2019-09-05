FROM python:3.6-alpine

COPY . /app

WORKDIR /app

RUN pip install -r requirements.txt
RUN apk add curl

HEALTHCHECK CMD curl --fail http://localhost:5000/ || exit 1
#unhealthy
#HEALTHCHECK CMD curl --fail http://localhost:5001/ || exit 1

CMD ["python", "app.py"]
