ARG BUILD_FROM
ARG BUILD_DATE
ARG BUILD_REF
ARG BUILD_VERSION
FROM $BUILD_FROM

# Install requirements for add-on
#RUN \
#  apk add --no-cache \
#    py3-pip \
#    python3

# Python 3 HTTP Server serves the current working dir
# So let's set it to our add-on persistent data directory.
WORKDIR /data

# Copy data for add-on
COPY rootfs /

RUN chmod a+x /app/run.sh

CMD [ "/bin/sh","/app/run.sh" ]
