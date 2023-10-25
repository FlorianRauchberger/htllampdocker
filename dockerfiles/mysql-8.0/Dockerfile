FROM mysql:8.0
#ENV MYSQL_ROOT_HOST=%
#FROM mysql:latest

# Update mysqld.cnf to allow connections from any host
#RUN echo "[mysqld]" >> /etc/mysql/mysql.conf.d/mysqld.cnf && \
#    echo "bind-address = 0.0.0.0" >> /etc/mysql/mysql.conf.d/mysqld.cnf
COPY grant-permissions.sql /docker-entrypoint-initdb.d/
