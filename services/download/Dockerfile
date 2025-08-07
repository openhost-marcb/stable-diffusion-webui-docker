FROM bash:alpine3.19

RUN echo "https://ftp.halifax.rwth-aachen.de/alpine/v3.19/main" > /etc/apk/repositories && \
    echo "https://ftp.halifax.rwth-aachen.de/alpine/v3.19/community" >> /etc/apk/repositories && \
    apk update && \
    apk add --no-cache parallel aria2

COPY . /docker
RUN chmod +x /docker/download.sh
ENTRYPOINT ["/docker/download.sh"]


