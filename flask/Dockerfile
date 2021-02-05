FROM python:3.7.2-stretch

WORKDIR /app

COPY . /app

#RUN apt update -y

#RUN apt-get install net-tools vim -y

RUN python3 -m pip install -r requirements.txt

EXPOSE 8080

#CMD ["uwsgi", "app.ini"]

CMD ["uwsgi", "--http-socket", ":8080", "--chdir", "/app", "--manage-script-name", "--mount", "/=run:app"]
