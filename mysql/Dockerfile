ARG IDOCKER_MYSQL_VERSION

FROM mysql:${IDOCKER_MYSQL_VERSION}

RUN echo "Asia/shanghai" > /etc/timezone;

RUN rm -rf /etc/localtime;
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

ADD ./conf.d/ /etc/mysql/conf.d
