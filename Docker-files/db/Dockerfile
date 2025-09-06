FROM mysql:8.0.33
LABEL Project="Vprofile"
LABEL Author="Kiran"

ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MYSQL_DATABASE="accounts"

# Copy SQL dump into MySQL init folder
ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
