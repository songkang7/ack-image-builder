#FROM alpine:3.10
FROM registry-cn-hangzhou.ack.aliyuncs.com/dev/alpine:3.20-update

ADD  https://releases.hashicorp.com/packer/1.7.9/packer_1.7.9_linux_amd64.zip /packer_1.7.9_linux_amd64.zip
ADD ./scripts /scripts
ADD ./config /config
RUN  unzip  packer_1.7.9_linux_amd64.zip && mv packer /bin/packer

ENTRYPOINT  ["packer", "build"]