FROM teamcity_teamcity
MAINTAINER Thushan Fernando <code@thushanfernando.com>
ADD buildAgent.properties TeamCity/buildAgent/conf/

RUN apt-get update && \
	apt-get install -y python python-pip python-dev libxml2-dev libxslt-dev libffi-dev libssl-dev 

RUN pip install lxml && pip install pyopenssl 

EXPOSE 8111 9090
ENTRYPOINT TeamCity/buildAgent/bin/agent.sh run
