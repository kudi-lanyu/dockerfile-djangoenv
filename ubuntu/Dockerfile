# Version: 0.0.1
FROM ubuntu:16.04
MAINTAINER meilida "mengliang@pku.edu.cn"
ENV REFRESHED_AT 2017-09-07
RUN ["apt-get", "update"]
RUN ["apt-get", "install", "-y", "python3.5"]
RUN ["apt-get", "install", "-y", "python3-pip"]

RUN ["pip3", "install", "-r", "./requirements.txt"]

# env tools and other software
RUN ["./env-tools.sh" ]

# create user

#基础文件部署
EXPOSE 8000
EXPOSE 8080
EXPOSE 9000
EXPOSE 9090
