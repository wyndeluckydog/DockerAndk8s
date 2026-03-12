FROM centos:7

# Install basic development tools
RUN yum update -y && \
    yum install -y epel-release && \
    yum install -y \
        curl \
        wget \
        git \
        nodejs \
        npm \
        python3 \
        python3-pip \
        bash \
        openssh-clients \
        ca-certificates && \
    yum clean all

# Install Docker CLI
RUN curl -fsSL https://get.docker.com -o get-docker.sh && \
    sh get-docker.sh && \
    rm get-docker.sh

# Create a non-root user
RUN useradd -m -s /bin/bash vscode

USER vscode
WORKDIR /workspaces
