ARG BUILD_FROM
FROM $BUILD_FROM

ENV LANG C.UTF-8

# Setup
RUN apk add --no-cache -U nodejs npm ffmpeg git \
    && cd / \
	&& git clone https://github.com/urkoin/ringhass \
	&& cd /ringhass \
    && npm install --unsafe-perm
	

# Build arugments
ARG BUILD_DATE
ARG BUILD_REF
ARG BUILD_VERSION
ARG BUILD_ARCH

# Labels
LABEL \
    io.hass.name="Rinhass Ring live view for Hassio" \
    io.hass.description="Rinhass Ring live view for Hassio" \
    io.hass.arch="${BUILD_ARCH}" \
    io.hass.type="addon" \
    io.hass.version=${BUILD_VERSION} \
    maintainer="Dani Manzaneque <danimanzaneque@gmail.com>" \
    org.label-schema.description="Easy integration of Amazon Dash buttons with Home Assistant instance" \
    org.label-schema.build-date=${BUILD_DATE} \
    org.label-schema.name="rinhass" \
    org.label-schema.schema-version="1.0" \
    org.label-schema.url="https://community.home-assistant.io/t/dasshio-amazon-dash-buttons-hass-io-add-on" \
    org.label-schema.usage="https://github.com/danimtb/dasshio/tree/master/README.md" \
    org.label-schema.vcs-ref=${BUILD_REF} \
    org.label-schema.vcs-url="https://github.com/urkoin/ringhass" \
    org.label-schema.vendor="Ring Hass.io Add-on"


CMD [ "/ringhass/run.sh" ]

