FROM node:lts-alpine

# Dependencias del sistema
RUN apk add --no-cache \
    bash git openssh \
    libc6-compat \
    python3 make g++ \
    tini

# Corepack / pnpm
RUN corepack enable && corepack prepare pnpm@latest --activate

USER node

ENTRYPOINT ["/sbin/tini", "--"]
