FROM ubuntu:focal as base
WORKDIR /usr/local/bin
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && \
    apt-get install -y apt-utils 2>&1 | grep -v "debconf: delaying package configuration, since apt-utils is not installed" && \
    apt-get install -y sudo

FROM base AS canary
ARG TAGS
RUN addgroup --gid 1000 adam
RUN adduser --gecos adam --uid 1000 --gid 1000 --disabled-password adam
WORKDIR /home/adam
COPY bootstrap.sh .
RUN chmod +x bootstrap.sh
CMD ["/bin/bash", "bootstrap.sh"]