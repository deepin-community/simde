# Helpful in communication with upstream about build/test issues

FROM debian:unstable

RUN apt-get update && apt-get upgrade -y && apt-get install -y --no-install-recommends \
  debhelper \
  cmake \
  git \
  ca-certificates \
  git-buildpackage \
  build-essential
WORKDIR /build
RUN gbp clone https://salsa.debian.org/med-team/simde.git
WORKDIR /build/simde
RUN gbp buildpackage
