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

CMD [ "/ringhass/run.sh" ]

