# Alternative Option 2: Direct PNPM Installation
FROM node:latest
ENV PNPM_HOME="/pnpm"
ENV PATH="$PNPM_HOME:$PATH"
RUN corepack enable

RUN corepack prepare pnpm@latest --activate

WORKDIR /workspace

# Install NestJS CLI and TypeScript globally
RUN pnpm add -g @nestjs/cli typescript

USER node

RUN  pnpm config set store-dir ~/.pnpm-store  

# Set default shell
SHELL ["/bin/bash", "-c"]

# Verify pnpm installation
RUN pnpm --version

# Keep container running
CMD ["sleep", "infinity"]