ARG MYSQL_IMAGE

FROM ${MYSQL_IMAGE}

RUN echo "Asia/shanghai" > /etc/timezone;

RUN rm -rf /etc/localtime;
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

ADD ./conf/ /etc/mysql/conf.d
