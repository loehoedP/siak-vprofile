FROM mysql:8.0.33
LABEL project="chelsea"
LABEL app="vprofile"
LABEL author="loehoedp"

ENV MYSQL_PASSWORD="vprodbpass"
ENV MYSQL_DATABASES="accounts"

ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql
