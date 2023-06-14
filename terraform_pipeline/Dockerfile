FROM ghcr.io/helmfile/helmfile:v0.150.0 AS helmfile_image
FROM docker.io/alpine:3.18

ENV HELM_PLUGINS=/usr/share/helm/plugins/

COPY --from=helmfile_image /usr/local/bin/helmfile /usr/bin/helmfile

RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories
RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories

RUN apk update
RUN apk add aws-cli jq kubectl helm terraform git sops bash
RUN helmfile init --force
