FROM elixir:1.9-alpine

RUN apk add --no-cache bash && \
  apk add --no-cache --virtual .build-deps openssl && \
  wget -q https://storage.googleapis.com/kubernetes-release/release/v1.8.11/bin/linux/amd64/kubectl \
    -O /usr/local/bin/kubectl && \
  chmod 755 /usr/local/bin/kubectl && \
  kubectl version --client && \
  apk del .build-deps
