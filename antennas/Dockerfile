FROM node:16-alpine
LABEL maintainer="jf.arseneau@gmail.com"

COPY . /antennas
WORKDIR "/antennas"
RUN \
    apk update \
    && apk add --no-cache --virtual .build-deps \
        libssl-dev \
        libyaml-0-2 \
RUN npm install

EXPOSE 5004
CMD ["npx", "--yes", "."]
