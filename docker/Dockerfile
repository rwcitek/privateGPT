FROM ubuntu:22.04
RUN apt-get update && \
    apt-get dist-upgrade -y
RUN apt-get install -y \
      python3-pip \
      ;

ADD     src /src
WORKDIR /src
RUN     pip3 install -r requirements.txt ; find /root/.cache/pip/ -type f -delete
RUN     mv example.env .env

WORKDIR /src/models
RUN     curl -O https://gpt4all.io/models/ggml-gpt4all-j-v1.3-groovy.bin



WORKDIR /src
COPY Dockerfile /


# include some tools for the interactive container
RUN     apt-get install -y less rsync vim curl tree file

