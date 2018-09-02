FROM ubuntu:18.04

RUN apt-get update
RUN apt-get install -y \
    python3 \
    python3-pip

# Only copy requirements upfront so we can minimize docker build times
# when source changes, but requirements do not
COPY src/requirements.txt /opt/aparkinson/websockets/src/requirements.txt
WORKDIR /opt/aparkinson/websockets/src/
RUN pip3 install -r requirements.txt

COPY src/ /opt/aparkinson/websockets/src/
