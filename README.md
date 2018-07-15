# `docker-jre-python`

Dockerfile setup with Java JRE and Python. All builds listed in this repository
are built on weekly basis by Travis CI.

## Builds

Currently only the following are included:

- Alpine (via `apk` only)
  - 3.8 + `openjdk8-jre` + `python2`
  - 3.8 + `openjdk8-jre` + `python3`
- Ubuntu (via `apt` only)
  - 18.04 + `openjdk-8-jre`+ `python2.7`
  - 18.04 + `openjdk-8-jre`+ `python3.6`
  - 18.04 + `openjdk-8-jre`+ `python3.7`
