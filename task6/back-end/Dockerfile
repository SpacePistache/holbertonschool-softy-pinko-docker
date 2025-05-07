FROM ubuntu:latest

RUN apt-get update && \
    apt-get install -y python3 python3-pip python3-venv

RUN python3 -m venv /opt/venv

RUN /opt/venv/bin/pip install --no-cache-dir flask flask-cors

ENV PATH="/opt/venv/bin:$PATH"

WORKDIR /app

COPY ./api.py /app/api.py

CMD ["python", "api.py"]

