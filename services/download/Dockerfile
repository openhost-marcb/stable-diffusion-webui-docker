FROM debian:bullseye-slim

RUN apt-get update && apt-get install -y parallel aria2
COPY . /docker
RUN chmod +x /docker/download.sh
ENTRYPOINT ["/docker/download.sh"]


