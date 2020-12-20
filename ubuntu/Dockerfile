FROM ubuntu:18.04
RUN apt update && \
    apt install openssh-server -y && \ 
    apt autoremove && \
    apt clean && \
    rm -rf /tmp/* /var/lib/apt/lists/* /var/tmp
RUN mkdir /run/sshd && mkdir /root/.ssh && chmod 700 /root/.ssh
RUN sed -i 's/^#PermitRootLogin .*/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN echo "root:root" | chpasswd
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
