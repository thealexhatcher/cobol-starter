FROM alpine:latest
RUN apk update \
    && apk upgrade \
    && apk add --no-cache git openssh sudo
RUN adduser -D vscode && mkdir -p /etc/sudoers.d \
    && echo "vscode ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/vscode \
    && chmod 0440 /etc/sudoers.d/vscode
USER vscode
RUN 
WORKDIR $HOME