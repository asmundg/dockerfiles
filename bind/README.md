# BIND docker image

Run the BIND DNS server in a docker container.

This is a totally simple forwarding bind container. To resolve zones,
mount a file containing zone configs at /etc/bind/named.conf.local:

    docker run --rm -p 53:53/udp asmundg/bind
