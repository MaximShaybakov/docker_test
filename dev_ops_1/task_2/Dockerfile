FROM ubuntu:jammy

WORKDIR /django_crud

RUN apt-get update && apt-get upgrade -y \
    apt-get install python3-pip \
    pip install requirements.txt \
    pip install django_filter

COPY . ./django_crud

ARG venv
ARG venv="${venv}"

EXPOSE 8080

CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]