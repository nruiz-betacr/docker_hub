FROM odoo:15.0
MAINTAINER Norlan Ruiz <nruiz@betasolutions.tech>

USER root

ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=America/Costa_Rica
ENV ODOO_VERSION 15.0

RUN apt update && apt install -y git
RUN git clone --branch ${ODOO_VERSION} --depth 1 --single-branch https://github.com/odoocr/l10n_cr.git /mnt/l10n_cr \
    && git clone --branch ${ODOO_VERSION} --depth 1 --single-branch https://github.com/odoocr/cabys.git /mnt/extra-addons

RUN python3 -m pip install --upgrade pip
RUN python3 -m pip install wheel
RUN python3 -m pip install -r /mnt/l10n_cr/requirements.txt

USER odoo
