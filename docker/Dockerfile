ARG VARIANT
FROM python:3$VARIANT
MAINTAINER Jean-Marc Astesana <admin@fathzer.com>

WORKDIR ./lichessbot

COPY . .

RUN python3 -m pip install --no-cache-dir -r requirements.txt

ENV LICHESS_BOT_DOCKER="true"
ENV PYTHONDONTWRITEBYTECODE=1

CMD python3 lichess-bot.py ${OPTIONS} --disable_auto_logging --config /engine/config.yml
