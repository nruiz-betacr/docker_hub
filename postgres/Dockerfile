FROM postgres:14
MAINTAINER Norlan Ruiz <nruiz@betasolutions.tech>

ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=America/Costa_Rica

RUN mkdir -p /var/lib/postgresql/data/pgdata
COPY ./postgres.conf /var/lib/postgresql/data/pgdata