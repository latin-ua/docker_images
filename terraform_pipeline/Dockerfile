FROM docker.io/hashicorp/terraform:1.4

RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories
RUN apk add aws-cli jq kubectl helm helmfile
