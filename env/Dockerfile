FROM ubuntu:focal
WORKDIR /usr/local/bin
ARG TAGS
RUN addgroup --gid 1000 adam
RUN adduser --gecos adam --uid 1000 --gid 1000 --disabled-password adam
USER adam
WORKDIR /home/adam

FROM new-machine
COPY ../bootstrap.sh /usr/local/bin
CMD chmod +x /usr/local/bin/bootstrap.sh
CMD ["./bootstrap.sh"]