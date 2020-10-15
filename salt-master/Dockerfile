FROM ubuntu:latest
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y wget gnupg
RUN wget -O - https://repo.saltstack.com/py3/ubuntu/20.04/amd64/3001/SALTSTACK-GPG-KEY.pub | apt-key add -
RUN echo "deb http://repo.saltstack.com/py3/ubuntu/20.04/amd64/latest focal main" | tee -a /etc/apt/sources.list.d/saltstack.list
RUN apt-get update
RUN apt-get install -y salt-master


EXPOSE 4505 4506

COPY setup.sh /opt/setup.sh

ENTRYPOINT ["cmd"]
