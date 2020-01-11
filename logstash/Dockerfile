FROM docker.elastic.co/logstash/logstash:7.4.2

EXPOSE 8080 12201

WORKDIR /usr/share/logstash/pipeline/

RUN logstash-plugin install --version 6.4.0 logstash-output-amazon_es

RUN rm -rf /usr/share/logstash/pipeline/*
RUN rm -rf /usr/share/logstash/config/*

COPY ./config/ /usr/share/logstash/config/
COPY ./pipeline/ /usr/share/logstash/pipeline/
