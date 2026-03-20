FROM node:24-bookworm-slim AS dev

RUN apt-get update && apt-get install -y --no-install-recommends \
    git curl bash ca-certificates \
    && rm -rf /var/lib/apt/lists/*

RUN npm install -g openclaw@latest

RUN mkdir -p /root/.openclaw

WORKDIR /workspace

EXPOSE 18789

CMD ["openclaw", "gateway"]
