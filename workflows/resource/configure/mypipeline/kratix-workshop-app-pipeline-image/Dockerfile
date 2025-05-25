FROM "alpine"

RUN apk update && apk add --no-cache yq kubectl

COPY scripts/* /usr/bin/
ADD resources resources

RUN chmod +x /usr/bin/*

# Fix for when running workshop on Windows machine
RUN apk update && apk add --no-cache dos2unix
RUN dos2unix /usr/bin/*

ENTRYPOINT []