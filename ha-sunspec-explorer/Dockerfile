FROM ghcr.io/home-assistant/base:latest

RUN apk add --no-cache \
    python3 \
    py3-pip

COPY app /app
COPY requirements.txt /
COPY run.sh /

RUN pip3 install --no-cache-dir --break-system-packages -r /requirements.txt

RUN chmod a+x /run.sh

CMD [ "/run.sh" ]