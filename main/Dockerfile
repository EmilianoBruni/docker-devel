# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #
#
# AUTHORS :  Emiliano Bruni (EB) <info@ebruni.it>
# DATE    :  2024-11-04
# PURPOSE :
#   a platform to develop [Perl](https://www.perl.org) apps.
#
#   This image is published in docker hub with handle: ebruni/devel
#
# USAGE:
#   docker build -t devel .
#
# UPDATES:
#   AUTHOR  DATE        VER  COMMENTS
#   EB      2024-11-04  2.1  Removed Term::ReadLine::Gnu for problem in debug and ignore git save.directory warnings
#   EB      2024-10-30  2.0  Update alpine to 3.20. Support for autocomplete in debug
#   EB      2021-09-29  1.3  Add Autoprereqs, Prereqs, PkgVersion
#   EB      2021-09-06  1.2  Add MinimumPerl to Dist::Zilla
#   EB      2021-08-29  1.1  Add Data::Printer
#   EB      2021-08-26  1.0  Initial Version
#
# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #
#

#
# this file is generated via docker-builder
#
# do not edit it directly
#
FROM alpine:3.20
LABEL maintainer="Emiliano Bruni <info@ebruni.it>"
ENV TZ=Europe/Rome

WORKDIR /usr/src
EXPOSE 3000 8080

RUN apk update && apk add --no-cache \
    build-base \
    perl-dev \
    perl-app-cpanminus \
    perl-module-build \
    perl-namespace-clean \
    perl-boolean \
    perl-json-maybexs \
    perl-test-fatal \
    perl-path-tiny \
    perl-moo \
    perl-file-find-rule \
    perl-number-compare \
    perl-text-glob \
    musl-dev \
    openssl \
    openssl-dev \
    zlib-dev \
    git \
    perl-data-printer \
    perl-term-readkey \
    perl-padwalker \
    readline-dev \
    tzdata \
  # remove safe.directory warning from git
  && git config --global --add safe.directory '*' \ 
  && cpanm --no-wget -n \
    Term::ReadLine::Perl \
  && rm -r /root/.cpanm \
  && apk del \
    readline-dev \
    ncurses-dev \
  && true

ARG NOW=not-set
LABEL org.opencontainers.image.authors="Emiliano Bruni <info@ebruni.it>"
LABEL org.opencontainers.image.created=$NOW
LABEL org.opencontainers.image.description="a platform to develop Perl apps."
LABEL org.opencontainers.image.documentation=https://github.com/EmilianoBruni/docker-devel/blob/master/README.pod
LABEL org.opencontainers.image.licenses=Artistic-2.0
LABEL org.opencontainers.image.source=https://github.com/EmilianoBruni/docker-devel/blob/master/main/Dockerfile
LABEL org.opencontainers.image.title=docker-devel
LABEL org.opencontainers.image.url=https://github.com/EmilianoBruni/docker-devel
LABEL org.opencontainers.image.version=2.1

CMD ["/bin/ash"]
