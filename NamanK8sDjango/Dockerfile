FROM python:3.10.0-alpine3.15

#RUN apk add --no-cache curl

WORKDIR /app1

COPY requirements.txt requirements.txt

RUN  pip install -r requirements.txt

COPY . /app1

EXPOSE 8000

#HEALTHCHECK --interval=30s --timeout=30s --start-period=30s --retries=3 \

#CMD curl -f http://localhost:8000 || exit 1

CMD [ "python","manage.py","runserver","0.0.0.0:8000" ]