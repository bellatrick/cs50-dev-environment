# Use a base image with a development environment
FROM mcr.microsoft.com/devcontainers/base:ubuntu-20.04

# Add the vscode user if not already present
RUN adduser --disabled-password --gecos "" vscode && \
    usermod -aG sudo vscode

# Set up workspace permissions
RUN mkdir -p /workspace && \
    chown -R vscode:vscode /workspace

# Set the working directory
WORKDIR /workspace

# Install dependencies (example)
RUN apt-get update && apt-get install -y build-essential python3-pip

# Set vscode as the default user
USER vscode
