FROM docker.elastic.co/logstash/logstash:7.4.0

EXPOSE 8080 12201

WORKDIR /usr/share/logstash/pipeline/

RUN rm -rf /usr/share/logstash/pipeline/*
RUN rm -rf /usr/share/logstash/config/*

COPY ./config/ /usr/share/logstash/config/
COPY ./pipeline/ /usr/share/logstash/pipeline/
