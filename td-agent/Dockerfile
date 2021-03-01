FROM debian:buster
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -y --no-install-recommends git curl ca-certificates sudo gnupg2
RUN curl -L https://toolbelt.treasuredata.com/sh/install-debian-buster-td-agent4.sh | sh
