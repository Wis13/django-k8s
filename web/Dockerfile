FROM python:3.11.1-alpine3.17

COPY . /app
WORKDIR /app

RUN python3 -m venv /opt/venv
RUN apk add postgresql-client build-base postgresql-dev

RUN /opt/venv/bin/pip install pip --upgrade && \
    /opt/venv/bin/pip install -r requirements.txt && \
    chmod +x entrypoint.sh

CMD [ "/app/entrypoint.sh" ]