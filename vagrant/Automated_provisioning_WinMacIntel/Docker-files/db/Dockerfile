FROM mysql:8.0.33
LABEL "PROJECT"="vprofile"
LABEL "NAME"="SAHJEB KHAN"

ENV MY_SQL_ROOT_PASSWORD="vprodbpass"
ENV MY_SQL_DATBASE="accounts"

ADD db_backup.sql docker_entrypoint-initdb.d/db_backup.sql
