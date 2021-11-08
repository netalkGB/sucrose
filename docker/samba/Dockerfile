FROM ubuntu:focal

RUN apt update 
RUN apt install samba -y

COPY ./smb.conf /etc/samba/smb.conf

EXPOSE 139
EXPOSE 445
EXPOSE 137/udp
EXPOSE 138/udp

CMD /usr/sbin/nmbd -D && /usr/sbin/smbd -FS --no-process-group
