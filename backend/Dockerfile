FROM python:3.7-slim

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
ENV PYTHONIOENCODING UTF-8

WORKDIR /usr/src/app
ADD ./backend_desafio/requirements.txt /usr/src/app
RUN pip install --upgrade pip  \
        && pip install --no-cache-dir -r requirements.txt
