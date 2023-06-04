FROM ubuntu:22.04
RUN apt-get update && \
    apt-get dist-upgrade -y
RUN apt-get install -y \
      python3-pip \
      ;

RUN     apt-get install -y less rsync vim curl

ADD     src src
WORKDIR src
RUN     pip3 install -r requirements.txt

WORKDIR models
RUN     curl -O https://gpt4all.io/models/ggml-gpt4all-j-v1.3-groovy.bin


