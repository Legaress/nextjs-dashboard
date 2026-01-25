FROM node:trixie-slim

RUN echo 'Acquire::ForceIPv4 "true";' > /etc/apt/apt.conf.d/99force-ipv4


RUN apt-get update \
 && apt-get install -y --no-install-recommends \
    build-essential \
    git \
    openssh-client \
 && rm -rf /var/lib/apt/lists/*

RUN npm install -g pnpm

USER node
