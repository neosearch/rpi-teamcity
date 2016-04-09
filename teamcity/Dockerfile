FROM anapsix/alpine-java:jdk
MAINTAINER Thushan Fernando <code@thushanfernando.com>
MAINTAINER pixelistik <code@pixelistik.de>

ENV TEAMCITY_VERSION_MAJOR 9
ENV TEAMCITY_VERSION_MINOR 1
ENV TEAMCITY_VERSION_BUILD 16

RUN wget -v https://download.jetbrains.com/teamcity/TeamCity-${TEAMCITY_VERSION_MAJOR}.${TEAMCITY_VERSION_MINOR}.${TEAMCITY_VERSION_BUILD}.tar.gz && \
    tar -xzvf TeamCity-${TEAMCITY_VERSION_MAJOR}.${TEAMCITY_VERSION_MINOR}.${TEAMCITY_VERSION_BUILD}.tar.gz && \
    rm TeamCity-${TEAMCITY_VERSION_MAJOR}.${TEAMCITY_VERSION_MINOR}.${TEAMCITY_VERSION_BUILD}.tar.gz

EXPOSE 8111 9090

ENV TEAMCITY_DATA_PATH /root/BuildServer
ENTRYPOINT ["TeamCity/bin/teamcity-server.sh","run"]
