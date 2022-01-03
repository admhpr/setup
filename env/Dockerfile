FROM ubuntu:focal as canary
WORKDIR /usr/local/bin
ARG TAGS
RUN addgroup --gid 1000 adam
RUN adduser --gecos adam --uid 1000 --gid 1000 --disabled-password adam
WORKDIR /home/adam
COPY bootstrap.sh /usr/local/bin
RUN chmod +x /usr/local/bin/bootstrap.sh
CMD ["./bootstrap.sh"]