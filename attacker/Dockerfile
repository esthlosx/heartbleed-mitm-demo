FROM kalilinux/kali-rolling
ADD heartleech /usr/bin/
ADD attacker.sh /root/ 
ADD mitmpcap.py /root/

RUN apt-get update && apt-get install -y \
        iputils-ping net-tools dsniff iproute2 bash isc-dhcp-client \
	traceroute dnsutils tcpdump \
	vim wget iptables mitmproxy

CMD ["echo 1 > /proc/sys/net/ipv4/ip_forward"]
CMD ["/bin/bash"]

 
