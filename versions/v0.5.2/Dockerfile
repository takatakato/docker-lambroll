FROM alpine:3.11.5

ENV LAMBROLL_VERSION=v0.5.2

RUN apk --no-cache add --virtual build-dependencies wget \
      && wget https://github.com/fujiwara/lambroll/releases/download/v0.5.2/lambroll_${LAMBROLL_VERSION}_linux_amd64.tar.gz \
      && tar -xvzf lambroll_${LAMBROLL_VERSION}_linux_amd64.tar.gz \
      && cp -p lambroll_${LAMBROLL_VERSION}_linux_amd64/lambroll /usr/local/bin \
      && rm -fr lambroll_${LAMBROLL_VERSION}_linux_amd64 \
      && rm -fr lambroll_${LAMBROLL_VERSION}_linux_amd64.tar.gz \
      && apk del --purge -r build-dependencies

ENTRYPOINT ["lambroll"]