ARG VARIANT
FROM python:3$VARIANT
MAINTAINER Jean-Marc Astesana <admin@fathzer.com>

ENV LICHESS_BOT_DOCKER="true"
ENV PYTHONDONTWRITEBYTECODE=1

WORKDIR ./lichessbot

COPY . .

RUN python3 -m pip install --no-cache-dir -r requirements.txt

RUN ln -s /engine/config.yml config.yml

CMD python3 lichess-bot.py ${OPTIONS} --disable_auto_logging
