# mysql debian Dockerfile
FROM debian

RUN apt-get -y upgrade

ENV MYSQL_USER=mysql \
    MYSQL_DATA_DIR=/var/lib/mysql \
    MYSQL_RUN_DIR=/run/mysqld \
    MYSQL_LOG_DIR=/var/log/mysql

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y mariadb-server && rm -rf /var/lib/apt/lists/*

EXPOSE 3306/tcp
#ENTRYPOINT ["/bin/sh", "-c", "/usr/bin/mysqld"]
