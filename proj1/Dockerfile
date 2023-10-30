#### update centoS version
## updated useradd cmd
## updated keygen

FROM centos:7

RUN yum install openssh-server -y
RUN yum install passwd -y

RUN useradd remote_user && \
    echo "remote_user:1234" | chpasswd && \
    mkdir /home/remote_user/.ssh && \
    chmod 700 /home/remote_user/.ssh

COPY remote-key.pub /home/remote_user/.ssh/authorized_keys

RUN chown remote_user:remote_user -R /home/remote_user/.ssh && \
   chmod 600 /home/remote_user/.ssh/authorized_keys
RUN ssh-keygen -A

#RUN yum update -y && yum install nginx -y
#CMD ["nginx", "-g", "daemon off;"]
#EXPOSE 80


