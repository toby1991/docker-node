FROM node:7.9.0

MAINTAINER Toby <t.post@hotmail.com>

ENV LANG C.UTF-8
ENV LANGUAGE C.UTF-8
ENV LC_ALL C.UTF-8
ENV PATH /root/bin:$PATH
ENV NLS_LANG American_America.AL32UTF8
ENV TIMEZONE America/Denver
ENV TERM xterm

RUN set -x \
    && apt-get -qq update \
    && apt-get install -qqy apt-utils \
    && apt-get -qq upgrade \
    && apt-get -qq dist-upgrade \
    && apt-get install -qqy \
        git \
        mercurial \
        rsync \
        subversion \
        sudo \
        wget \

    # install npm packages
    && npm install --silent -g \
        gulp-cli \
        grunt-cli \
        bower \
        markdown-styles \
        cnpm \
        yarn \
        laravel-echo-server



VOLUME /src
WORKDIR /src

CMD ["/run-as-user", "/usr/local/bin/npm"]
