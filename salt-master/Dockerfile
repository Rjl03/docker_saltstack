FROM ubuntu:latest

RUN apt-get update \
  && apt-get install -y wget \
  && wget --no-check-certificate -O - https://repo.saltstack.com/py3/ubuntu/20.04/amd64/latest/SALTSTACK-GPG-KEY.pub \
  && echo "deb http://repo.saltstack.com/py3/ubuntu/20.04/amd64/latest focal main" | tee -a /etc/apt/sources.list \
  && apt-get update \
  && apt-get install -y salt-master

COPY setup.sh /opt/setup.sh
ENTRYPOINT ["sh", "/opt/setup.sh"]
