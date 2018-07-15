ARG UBUNTU_VERS=
FROM ubuntu:${UBUNTU_VERS}

ARG JAVA_VERS=
ARG PYTHON_MAJOR_NUM=
ARG PYTHON_MINOR_NUM=

RUN apt-get update && apt-get install -y --no-install-recommends \
    openjdk-${JAVA_VERS}-jre \
    python${PYTHON_MAJOR_NUM}.${PYTHON_MINOR_NUM} \
    && if [ "${PYTHON_MAJOR_NUM}" = "3" ]; then \
    apt-get install -y --no-install-recommends python${PYTHON_MAJOR_NUM}-pip; \
    else \
    apt-get install -y --no-install-recommends python-pip; \
    fi \
    && rm -rf /var/lib/apt/lists/*
