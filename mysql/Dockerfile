# mysql debian Dockerfile
FROM debian

RUN apt-get update
RUN apt-get -y upgrade

# install maria-db-server
RUN echo 'mariadb-server mariadb-server/root_password  password mypassword' | debconf-set-selections
RUN echo 'mariadb-server mariadb-server/root_password_again password mypassword' | debconf-set-selections
RUN apt-get install mariadb-server -y

EXPOSE 3306

CMD /usr/bin/mysqld &&
