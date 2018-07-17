ARG UBUNTU_VERS=
FROM ubuntu:${UBUNTU_VERS}

ARG JAVA_VERS=
ARG PYTHON_MAJOR_NUM=
ARG PYTHON_MINOR_NUM=

RUN set -e \
    && apt-get update && apt-get install -y --no-install-recommends \
    openjdk-${JAVA_VERS}-jre \
    python${PYTHON_MAJOR_NUM}.${PYTHON_MINOR_NUM} \
    && PYTHON_PATH=`which python${PYTHON_MAJOR_NUM}.${PYTHON_MINOR_NUM}` \
    && if [ "${PYTHON_MAJOR_NUM}" = "3" ]; then \
    apt-get install -y --no-install-recommends python${PYTHON_MAJOR_NUM}-pip \
    && update-alternatives --install /usr/local/bin/python python "${PYTHON_PATH}" 1 \
    && update-alternatives --install /usr/local/bin/python3 python3 "${PYTHON_PATH}" 1 \
    ; \
    else \
    apt-get install -y --no-install-recommends python-pip \
    && update-alternatives --install /usr/local/bin/python python "${PYTHON_PATH}" 1 \
    && update-alternatives --install /usr/local/bin/python2 python2 "${PYTHON_PATH}" 1 \
    ; \
    fi \
    && rm -rf /var/lib/apt/lists/*
