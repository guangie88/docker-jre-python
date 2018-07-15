ARG ALPINE_VERS=
FROM alpine:${ALPINE_VERS}

ARG JAVA_VERS=
ARG PYTHON_VERS=

RUN apk --no-cache add \
    openjdk${JAVA_VERS}-jre \
    python${PYTHON_VERS}
