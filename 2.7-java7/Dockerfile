FROM openjdk:7-jre
LABEL maintainer="felixlohmeier@opencultureconsulting.com"
# OpenRefine 2.7

ENV OR_URL https://github.com/OpenRefine/OpenRefine/releases/download/2.7/openrefine-linux-2.7.tar.gz

WORKDIR /app

RUN wget -qO- ${OR_URL} | tar -xz --strip 1

VOLUME /data
WORKDIR /data

EXPOSE 3333

ENTRYPOINT ["/app/refine"]
CMD ["-i", "0.0.0.0", "-d", "/data"]
