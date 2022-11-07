# build this image docker build xterm .
# run this image:
# docker run --rm -i -t  -v ${HOME}:${HOME} buildroot:18.04 bash
# or
# . ./run
#
FROM ubuntu:18.04
RUN apt-get -y update
RUN apt-get -y install xterm
RUN apt-get -y install xauth
RUN apt-get -y install sudo

RUN apt -y install rsync wget unzip build-essential git bc swig libncurses-dev \
	libpython3-dev libssl-dev python3-distutils cpio xxd

# create a normal user so we're not running as root
RUN export uid=1000 gid=1000 && \
    mkdir -p /home/developer && \
    echo "developer:x:${uid}:${gid}:Developer,,,:/home/developer:/bin/bash" >> /etc/passwd && \
    echo "developer:x:${uid}:" >> /etc/group && \
    echo "developer ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/developer && \
    chmod 0440 /etc/sudoers.d/developer && \
    chown ${uid}:${gid} -R /home/developer

# switch to user
USER developer
ENV HOME /home/developer

CMD xterm
