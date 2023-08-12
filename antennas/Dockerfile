FROM node:16-alpine
LABEL maintainer="jf.arseneau@gmail.com"
RUN \
    apk update \
    && apk add --no-cache --virtual .build-deps \
        yaml
        openssl-dev
COPY . /antennas
WORKDIR "/antennas"
RUN npm install

EXPOSE 5004
CMD ["npx", "--yes", "."]
