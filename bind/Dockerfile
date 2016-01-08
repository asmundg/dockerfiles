FROM debian:jessie

RUN apt-get update && \
    apt-get install -y --no-install-recommends bind9
CMD ["named", "-f"]
EXPOSE 53
