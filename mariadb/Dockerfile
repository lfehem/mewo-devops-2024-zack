FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y mariadb-server && \
    apt-get clean && \
    useradd -ms /bin/bash mysqluser && \
    chown -R mysqluser:mysqluser /var/lib/mysql

USER mysqluser

EXPOSE 3306

CMD ["mysqld"]
