FROM debian:jessie
MAINTAINER John Downey <jdowney@gmail.com>

ENV RUST_VERSION 1.6.0

RUN apt-get update && apt-get install -y \
  build-essential \
  ca-certificates \
  curl \
  --no-install-recommends \
  && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /opt/rust-$RUST_VERSION \
  && curl -sSL https://static.rust-lang.org/dist/rust-$RUST_VERSION-x86_64-unknown-linux-gnu.tar.gz | tar -xvz -C /opt/rust-$RUST_VERSION --strip-components 1 \
  && cd /opt/rust-$RUST_VERSION \
  && ./install.sh \
