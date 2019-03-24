#Download base image ubuntu 18.04
FROM ubuntu:18.04
RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get install -f
RUN apt-get clean
RUN apt-get -y autoremove

# List of network tools obtained from: https://geekflare.com/linux-networking-commands/
# Install tools below
RUN apt-get -y install nano
# install `dnsutils` to use `dig`
RUN apt-get -y install dnsutils
# remove current /etc/resolve.conf
RUN echo '' > /etc/resolv.conf
# add nameserver
RUN echo "nameserver 1.1.1.1" >> /etc/resolv.conf
RUN echo "nameserver 1.0.0.1" >> /etc/resolv.conf
RUN echo "nameserver 8.8.8.8" >> /etc/resolv.conf
RUN echo "nameserver 8.4.4.8" >> /etc/resolv.conf
# install `inetutils-ping` to use `ping`
RUN apt-get -y install inetutils-ping
# install `net-tools` to use `ifconfig`
RUN apt-get -y install net-tools
RUN apt-get -y install traceroute
RUN apt-get -y install whois
RUN apt-get -y install ssh
RUN apt-get -y install nmap
RUN apt-get -y install netcat
RUN apt-get -y install tcpdump