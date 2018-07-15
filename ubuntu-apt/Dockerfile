ARG UBUNTU_VERS=
FROM ubuntu:${UBUNTU_VERS}

ARG JAVA_VERS=
ARG PYTHON_VERS=

RUN apt-get update && apt-get install -y --no-install-recommends \
    openjdk-${JAVA_VERS}-jre \
    python${PYTHON_VERS} \
    && rm -rf /var/lib/apt/lists/*
