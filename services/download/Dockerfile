FROM bash:alpine3.19

RUN sed -i 's/dl-cdn.alpinelinux.org/ftp.halifax.rwth-aachen.de\/alpine/' /etc/apk/repositories && \
    apk update && \
    apk add parallel aria2
COPY . /docker
RUN chmod +x /docker/download.sh
ENTRYPOINT ["/docker/download.sh"]

