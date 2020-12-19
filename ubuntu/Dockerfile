FROM ubuntu:18.04
RUN apt update && \
    apt install openssh-server -y && \ 
    apt autoremove && \
    apt clean && \
    rm -rf /tmp/* /var/lib/apt/lists/* /var/tmp
RUN mkdir /run/sshd
RUN echo "root:root" | chpasswd
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
