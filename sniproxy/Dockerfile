FROM debian:jessie

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
      automake \
      build-essential \
      ca-certificates \
      git \
      gettext \
      libev-dev \
      libev-dev \
      libpcre3-dev \
      libudns-dev \
      pkg-config && \
    mkdir -p /usr/src/ && \
    cd /usr/src && \
    git clone -b 0.4.0 https://github.com/dlundquist/sniproxy.git && \
    cd sniproxy && \
    ./autogen.sh && \
    ./configure && \
    make install && \
    apt-get purge -y automake build-essential git pkg-config && \
    apt-get autoremove -y
COPY sniproxy.conf /etc/
CMD ["sniproxy", "-f"]
EXPOSE 80 443
