FROM ubuntu

ARG DEBIAN_FRONTEND=noninteractive
ENV TZ="Europe/Vilnius"

RUN apt update && apt install -y python3 python3-pip docker.io software-properties-common
RUN add-apt-repository --yes --update ppa:ansible/ansible
RUN apt install -y ansible

RUN pip3 install docker

COPY playbook.yml /opt/playbook.yml

RUN ansible-galaxy collection install community.docker
