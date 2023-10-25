FROM mysql:5.7
#ENV MYSQL_ROOT_HOST=%

# Update mysqld.cnf to allow connections from any host
RUN echo "[mysqld]" >> /etc/mysql/mysql.conf.d/mysqld.cnf && \
    echo "bind-address = 0.0.0.0" >> /etc/mysql/mysql.conf.d/mysqld.cnf
