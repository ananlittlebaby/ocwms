FROM mysql:8.0.24

MAINTAINER lengleng(wangiegie@gmail.com)

ENV TZ=Asia/Shanghai

RUN ln -sf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

COPY ./wms.sql /docker-entrypoint-initdb.d

COPY ./wms_codegen.sql /docker-entrypoint-initdb.d

COPY ./wms_config.sql /docker-entrypoint-initdb.d

COPY ./wms_job.sql /docker-entrypoint-initdb.d
