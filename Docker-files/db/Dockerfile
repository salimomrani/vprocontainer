FROM mysql:8.0.33 
ENV MYSQL_ROOT_PASSWORD=root

ENV MYSQL_DATABASE="accounts"
ENV MYSQL_PASSWORD="vprodbpass"
ENV MYSQL_USER="root"

COPY db_backup.sql /docker-entrypoint-initdb.d/


# The init.sql file will be executed when the container is started for the first time.