FROM node:16

# Installe curl et kubectl
RUN apt-get update && apt-get install -y curl apt-transport-https gnupg && \
    curl -fsSL https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key add - && \
    echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | tee -a /etc/apt/sources.list.d/kubernetes.list && \
    apt-get update && \
    apt-get install -y kubectl

# Installe Docker CLI si nécessaire
RUN apt-get install -y docker.io
