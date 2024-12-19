FROM ubuntu:latest
RUN apt update -y
RUN apt install -y bind9 dnsutils
COPY named.conf.local /etc/bind/
COPY db.asa.br /etc/bind/
EXPOSE 53/tcp 53/udp
CMD ["/usr/sbin/named", "-g", "-c", "/etc/bind/named.conf", "-u", "bind"]
