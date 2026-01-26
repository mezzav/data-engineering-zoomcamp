FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

COPY --from=ghcr.io/astral-sh/uv:latest /uv /bin/

ARG TERRAFORM_VERSION=1.14.3
ARG COMPOSE_VERSION=1.29.2

RUN wget -q -O terraform.zip https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_arm64.zip && \
    unzip terraform.zip && \
    mv terraform /usr/local/bin && \
    chmod +x /usr/local/bin/terraform && \
    rm terraform.zip

RUN curl -L "https://github.com/docker/compose/releases/download/${COMPOSE_VERSION}/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose && \
    chmod +x /usr/local/bin/docker-compose

WORKDIR /workspaces/hw1

ENTRYPOINT ["/bin/bash"]
