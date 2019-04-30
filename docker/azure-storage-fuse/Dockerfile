FROM ubuntu:18.04

LABEL maintainer="chaimeliyah@gmail.com"

# create and set working directory
RUN wget https://packages.microsoft.com/config/ubuntu/16.04/packages-microsoft-prod.deb \
 && dpkg -i packages-microsoft-prod.deb \
 && apt-get update && apt-get install blobfuse fuse \
 && apt-get clean -y \
 && apt-get autoremove -y \
 && rm -rf /var/lib/apt/lists/*

# start app
CMD "/bin/bash"
