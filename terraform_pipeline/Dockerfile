FROM docker.io/alpine:3.18

ENV HELM_PLUGINS=/usr/share/helm/plugins/

RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories
RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories
RUN apk update
RUN apk add aws-cli jq kubectl helm helmfile terraform git sops bash
RUN helmfile init --force
