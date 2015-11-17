# VERSION 0.0.1
# AUTHOR:         Nicolas Lamirault <nicolas.lamirault@gmail.com>
# DESCRIPTION:    portefaix/clair

FROM portefaix/base:3.2
MAINTAINER Nicolas Lamirault <nicolas.lamirault@gmail.com>

ENV CLAIR_VERSION v0.0.1
ENV GOPATH /go
ENV GO15VENDOREXPERIMENT 1

RUN apk add --update build-base go git mercurial bzr

RUN mkdir -p /go/src/github.com/coreos && cd /go/src/github.com/coreos && \
    git clone https://github.com/coreos/clair.git -b ${CLAIR_VERSION} && \
    cd clair && \
    mkdir src && mv vendor/* src/ && mv src vendor && \
    GOPATH=/go:/go/src/github.com/coreos/clair/vendor go install -v && \
    cp /go/bin/clair / && \
    apk del --purge build-base nodejs go git mercurial && \
    rm -rf /go /tmp/* /var/cache/apk/* /root/.n*
RUN mkdir /db

VOLUME ["/db"]

EXPOSE 6060 6061

CMD ["/clair"]
