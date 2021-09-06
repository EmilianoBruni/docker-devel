# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #
#
# AUTHOR  :  Emiliano Bruni <info@ebruni.it>
# DATE    :  2021-08-26
# PURPOSE :
#   a platform to develop [Perl](https://www.perl.org) apps.
#
#   This image is published in docker hub with handle: ebruni/devel
#
# USAGE:
#   docker build -t devel .
#
# UPDATES:
#   AUTHOR          DATE        VERSION   COMMENTS
#   Emiliano Bruni  2021-09-06  1.2       Add MinimumPerl to Dist::Zilla
#   Emiliano Bruni  2021-08-29  1.1       Add Data::Printer
#   Emiliano Bruni  2021-08-26  1.0       Initial Version
#
# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #
#

#
# this file is generated via docker-builder
#
# do not edit it directly
#
FROM alpine:3.14
MAINTAINER Emiliano Bruni <info@ebruni.it>

WORKDIR /usr/src
EXPOSE 3000 8080

RUN apk update && apk add --no-cache \
    make \
    gcc \
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
  && cpanm --no-wget \
    Data::Printer \
  && rm -r /root/.cpanm \
 && apk add --no-cache \
    musl-dev \
    g++ \
&& cpanm --no-wget --notest \
    Dist::Zilla \
    Dist::Zilla::Plugin::ChangelogFromGit::CPAN::Changes \
    Dist::Zilla::Plugin::GithubMeta \
    Dist::Zilla::Plugin::MinimumPerlFast \
    Dist::Zilla::Plugin::MinimumPerl \
    Dist::Zilla::Plugin::PodWeaver \
    Dist::Zilla::Plugin::ReadmeAnyFromPod \
    Dist::Zilla::Plugin::Regenerate::AfterReleasers \
    Dist::Zilla::PluginBundle::Starter::Git \
  && rm -r /root/.cpanm \
  && true

ARG NOW=not-set
LABEL org.opencontainers.image.authors="Emiliano Bruni <info@ebruni.it>"
LABEL org.opencontainers.image.created=$NOW
LABEL org.opencontainers.image.description="a platform to develop Perl apps."
LABEL org.opencontainers.image.documentation=https://github.com/EmilianoBruni/docker-devel/blob/master/README.pod
LABEL org.opencontainers.image.licenses=Artistic-2.0
LABEL org.opencontainers.image.source=https://github.com/EmilianoBruni/docker-devel/blob/master/dzil/Dockerfile
LABEL org.opencontainers.image.title=docker-devel
LABEL org.opencontainers.image.url=https://github.com/EmilianoBruni/docker-devel
LABEL org.opencontainers.image.version=1.2-dzil

CMD ["/bin/ash"]
