FROM postgres:15-alpine

# Postgres settings
ENV POSTGRES_PASSWORD="pass"

# Point Postgres data files to a persistent location inside the container
ENV PGDATA="/data"

# CKAN settings
ENV CKAN_POSTGRES_DB="ckan"
ENV CKAN_POSTGRES_USER="ckan_default"
ENV CKAN_POSTGRES_USER_PWD="pass"

ENV CKAN_DATASTORE_POSTGRES_DB="datastore"
ENV CKAN_DATASTORE_POSTGRES_READ_USER="datastore_read"
ENV CKAN_DATASTORE_POSTGRES_READ_PWD="pass"
ENV CKAN_DATASTORE_POSTGRES_WRITE_USER="datastore_write"
ENV CKAN_DATASTORE_POSTGRES_WRITE_PWD="pass"

ARG CKAN_VERSION="2.10"
ENV CKAN_VERSION=${CKAN_VERSION}

ADD docker-entrypoint-initdb.d /docker-entrypoint-initdb.d
