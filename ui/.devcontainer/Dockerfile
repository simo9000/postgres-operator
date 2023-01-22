FROM registry.opensource.zalan.do/library/alpine-3.15:latest
LABEL maintainer="Team ACID @ Zalando <team-acid@zalando.de>"

RUN \
  apk add --no-cache \
    alpine-sdk \
    autoconf \
    automake \
    ca-certificates \
    libffi-dev \
    libtool \
    python3 \
    python3-dev \
    zlib-dev \
    && \
  python3 -m ensurepip && \
  rm -r /usr/lib/python*/ensurepip && \
  pip3 install --upgrade \
    gevent \
    jq \
    pip \
    setuptools \
    && \
  rm -rf \
    /root/.cache \
    /tmp/* \
    /var/cache/apk/*