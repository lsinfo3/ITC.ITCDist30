FROM million12/typo3-flow-neos-abstract:latest
MAINTAINER Marcin Ryzycki marcin@m12.io

ENV DB_PORT_3306_TCP_ADDR 172.17.42.1
ENV DB_PORT_3306_TCP_PORT 3306
ENV DB_ENV_MARIADB_USER itc2018
ENV T3APP_NAME itc30
ENV T3APP_VHOST_NAMES "itc30.org www.itc30.org"

ENV T3APP_BUILD_REPO_URL https://github.com/lsinfo3/ITC.ITCDist30.git
ENV T3APP_BUILD_BRANCH master
ENV T3APP_NEOS_SITE_PACKAGE Itc.ITeleTraffic
ENV FLOW_CONTEXT=Production

ADD config.json /root/.composer/config.json

VOLUME ["/srv/itc30/Resources"]

RUN . /build-typo3-app/pre-install-typo3-app.sh
