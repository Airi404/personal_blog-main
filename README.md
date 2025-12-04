1º Parte
Realizamos el Dockerfile y la primera parte del compose 
services:
  web:
    build: .
    command: >
      sh -c "python manage.py migrate --noinput && 
      python manage.py runserver 0.0.0.0:8000"
    ports:
      - "8000"
