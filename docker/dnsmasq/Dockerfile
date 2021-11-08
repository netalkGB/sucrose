FROM ubuntu:focal

RUN apt update 
RUN apt install -y dnsmasq 

EXPOSE 53 53/udp

COPY ./dnsmasq.conf /etc/dnsmasq.conf
COPY ./hosts.dnsmasq /etc/hosts.dnsmasq

CMD ["dnsmasq", "-k"]
