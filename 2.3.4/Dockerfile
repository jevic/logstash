FROM openjdk:8-jre
MAINTAINER jieyang <admin@jevic.cn>
ENV EFRESHED_AT 2017-12-25
ENV LOGSTASH_VERSION 2.3.4
ENV TZ Asia/Shanghai

RUN cd /opt/ \
    && wget http://ftp.kernel.yunfan.com/docker/logstash/logstashIPIP.tar.gz \
    && tar zxf logstashIPIP.tar.gz \
    && mv logstashIPIP logstash \
    && rm -rf logstashIPIP.tar.gz

ENV PATH /opt/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
WORKDIR /opt/logstash/etc

COPY docker-entrypoint.sh /

ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["-e", ""]
