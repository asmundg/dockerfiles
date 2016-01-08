# Sniproxy docker image

Run the SNIProxy HTTP server in a docker container.

SNIProxy proxies both HTTP and HTTPS, supporting the latter without
having to decrypt the communication. This requires that the client
supports SNI.

The server will default proxy any connection, using the client's Host
header to resolve and contact the wanted server.

    docker run --rm -p 80:80 -p 443:443 asmundg/sniproxy
