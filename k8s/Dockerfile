FROM jenkins/inbound-agent:latest

# Installer curl, kubectl, Node.js et JDK
USER root

RUN apt-get update && \
    apt-get install -y curl gnupg2 lsb-release apt-transport-https ca-certificates

# Installer kubectl
RUN curl -LO "https://dl.k8s.io/release/$(curl -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" && \
    chmod +x kubectl && \
    mv kubectl /usr/local/bin/

# Installer Node.js 16
RUN curl -fsSL https://deb.nodesource.com/setup_16.x | bash - && \
    apt-get install -y nodejs

# Installer OpenJDK 17
RUN apt-get install -y openjdk-17-jdk

USER jenkins

