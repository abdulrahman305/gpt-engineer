FROM python:3.13.0a4-slim

RUN apt-get update \
 && apt-get install -y sudo tk tcl gcc curl

WORKDIR /app

COPY . .
COPY docker/entrypoint.sh ./entrypoint.sh

RUN sudo pip install -e .

ENTRYPOINT ["bash", "/app/entrypoint.sh"]
