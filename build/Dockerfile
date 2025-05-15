FROM alpine:3.10

ADD  https://releases.hashicorp.com/packer/1.12.0/packer_1.12.0_linux_amd64.zip /packer_1.12.0_linux_amd64.zip
ADD ./scripts /scripts
ADD ./config /config
RUN  unzip  packer_1.12.0_linux_amd64.zip && mv packer /bin/packer
RUN packer plugins install github.com/hashicorp/alicloud v1.1.2


ENTRYPOINT  ["packer", "build"]