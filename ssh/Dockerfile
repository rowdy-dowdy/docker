
FROM ubuntu:latest

RUN apt update && apt install  openssh-server sudo -y

RUN useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 admin 

RUN  echo 'admin:123456' | chpasswd

RUN service ssh start

EXPOSE 22

CMD ["/usr/sbin/sshd","-D"]
