FROM amazon/aws-cli:latest

RUN yum update -y && \
yum install -y tar gzip

RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash

ENV HOME /root

ENV NVM_DIR "$HOME/.nvm"

RUN source "$NVM_DIR/nvm.sh" && nvm install --lts

COPY entrypoint.sh /

ENTRYPOINT ["/entrypoint.sh"]
