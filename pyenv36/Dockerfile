FROM ubuntu:16.04

MAINTAINER theolyu

ADD sources.list /etc/apt/

RUN apt-get update \
&& apt-get install gcc -y\
&& apt-get install g++ -y\
&& apt-get install gdb -y\
&& apt-get install python-software-properties -y\
&& apt-get install software-properties-common -y\
&& add-apt-repository ppa:deadsnakes/ppa -y\
&& apt-get update\
&& apt-get install python3.6 -y\
&& rm /usr/bin/python\
&& ln -s /usr/bin/python3.6 /usr/bin/python\
&& rm /usr/bin/python3\
&& ln -s /usr/bin/python3.6 /usr/bin/python3\
&& apt-get install python3-pip -y\
&& pip3 install pip -U\
&& rm /usr/bin/pip3 \
&& ln -s -f /usr/local/bin/pip3 /usr/bin/pip3\
&& ln -s -f /usr/local/bin/pip3 /usr/bin/pip\
&& pip config set global.index-url https://mirrors.aliyun.com/pypi/simple/ \
&& apt-get install vim -y
