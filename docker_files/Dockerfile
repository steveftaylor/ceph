FROM ubuntu:14.04

RUN groupadd -g 1375737880 build
RUN useradd -d /home/build -m -s /bin/bash -u 1375737880 -g 1375737880 build
# Set the locale
RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

RUN apt-get update && apt-get install -y sudo
RUN echo 'build ALL=(ALL) NOPASSWD: ALL' >> /etc/sudoers
RUN echo 'Defaults:build        !requiretty' >> /etc/sudoers

ENV HOME /home/build
USER build

CMD ["/bin/bash"]
