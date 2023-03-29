FROM mcr.microsoft.com/devcontainers/base:bullseye

WORKDIR /root

RUN apt update
RUN apt install -y --no-install-recommends \
    racket \
    libjpeg62 \
    libgtk2.0-dev \
    xvfb

RUN raco pkg install --auto --force racket-langserver || echo racket-langserver installed but had some problems.

ENV DISPLAY=:0
