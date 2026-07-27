mtech@programming-lab-Veriton-S2690G:~$ ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute 
       valid_lft forever preferred_lft forever
2: enp2s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
    link/ether 88:ae:dd:28:40:4a brd ff:ff:ff:ff:ff:ff
    inet 10.10.1.106/16 brd 10.10.255.255 scope global dynamic noprefixroute enp2s0
       valid_lft 41307sec preferred_lft 41307sec
    inet6 fe80::b432:299c:6c6:194a/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever
       
mtech@programming-lab-Veriton-S2690G:~$ sudo iftop -i lo
interface: lo
IP address is: 127.0.0.1
IPv6 address is: ::1
MAC address is: 00:00:00:00:00:00
mtech@programming-lab-Veriton-S2690G:~$ sudo iftop -i enp2s0
interface: enp2s0
IP address is: 10.10.1.106
MAC address is: 88:ae:dd:28:40:4a

mtech@programming-lab-Veriton-S2690G:~$ ping -c 5 10.10.1.83
PING 10.10.1.83 (10.10.1.83) 56(84) bytes of data.
64 bytes from 10.10.1.83: icmp_seq=1 ttl=64 time=0.702 ms
64 bytes from 10.10.1.83: icmp_seq=2 ttl=64 time=0.479 ms
64 bytes from 10.10.1.83: icmp_seq=3 ttl=64 time=1.02 ms
64 bytes from 10.10.1.83: icmp_seq=4 ttl=64 time=0.185 ms
64 bytes from 10.10.1.83: icmp_seq=5 ttl=64 time=0.912 ms

--- 10.10.1.83 ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4104ms
rtt min/avg/max/mdev = 0.185/0.659/1.019/0.300 ms

mtech@programming-lab-Veriton-S2690G:~$ netstat -u
Active Internet connections (w/o servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
udp        0      0 programming-lab-:bootpc _gateway:bootps         ESTABLISHED
mtech@programming-lab-Veriton-S2690G:~$ netstat -t
Active Internet connections (w/o servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
tcp        0      0 programming-lab-V:51618 93.243.107.34.bc.:https ESTABLISHED
tcp        0      0 programming-lab-V:37146 lb-140-82-113-26-:https ESTABLISHED

mtech@programming-lab-Veriton-S2690G:~$ whois google
% IANA WHOIS server
% for more information on IANA, visit http://www.iana.org
% This query returned 1 object

domain:       GOOGLE

organisation: Charleston Road Registry Inc.
address:      1600 Amphitheatre Parkway
address:      Mountain View CA 94043
address:      United States of America (the)

contact:      administrative
name:         TLD Admin
organisation: Google Inc.
address:      111 8th Avenue
address:      New York NY 10011
address:      United States of America (the)
phone:        +1 404 978 8419
fax-no:       +1 650 492 5631
e-mail:       iana-contact@google.com

contact:      technical
name:         TLD Engineering
organisation: Google Inc.
address:      76 Ninth Avenue, 4th Floor
address:      New York NY 10011
address:      United States of America (the)
phone:        +1 404 978 8419
fax-no:       +1 650 492 5631
e-mail:       crr-tech@google.com

nserver:      NS-TLD1.CHARLESTONROADREGISTRY.COM 2001:4860:4802:32:0:0:0:69 216.239.32.105
nserver:      NS-TLD2.CHARLESTONROADREGISTRY.COM 2001:4860:4802:34:0:0:0:69 216.239.34.105
nserver:      NS-TLD3.CHARLESTONROADREGISTRY.COM 2001:4860:4802:36:0:0:0:69 216.239.36.105
nserver:      NS-TLD4.CHARLESTONROADREGISTRY.COM 2001:4860:4802:38:0:0:0:69 216.239.38.105
nserver:      NS-TLD5.CHARLESTONROADREGISTRY.COM 2001:4860:4805:0:0:0:0:69 216.239.60.105
ds-rdata:     6125 8 2 80f8b78d23107153578bad3800e9543500474e5c30c29698b40a3db23ed9da9f

whois:        

status:       ACTIVE
remarks:      Registration information: https://www.registry.google

created:      2014-09-04
changed:      2025-04-11
source:       IANA

mtech@programming-lab-Veriton-S2690G:~$ whois google.com
   Domain Name: GOOGLE.COM
   Registry Domain ID: 2138514_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.markmonitor.com
   Registrar URL: http://www.markmonitor.com
   Updated Date: 2019-09-09T15:39:04Z
   Creation Date: 1997-09-15T04:00:00Z
   Registry Expiry Date: 2028-09-14T04:00:00Z
   Registrar: MarkMonitor Inc.
   Registrar IANA ID: 292
   Registrar Abuse Contact Email: abusecomplaints@markmonitor.com
   Registrar Abuse Contact Phone: +1.2086851750
   Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
   Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
   Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
   Domain Status: serverDeleteProhibited https://icann.org/epp#serverDeleteProhibited
   Domain Status: serverTransferProhibited https://icann.org/epp#serverTransferProhibited
   Domain Status: serverUpdateProhibited https://icann.org/epp#serverUpdateProhibited
   Name Server: NS1.GOOGLE.COM
   Name Server: NS2.GOOGLE.COM
   Name Server: NS3.GOOGLE.COM
   Name Server: NS4.GOOGLE.COM
   DNSSEC: unsigned
   URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
>>> Last update of whois database: 2026-07-13T04:30:54Z <<<

mtech@programming-lab-Veriton-S2690G:~$ nslookup google.com
;; communications error to 127.0.0.53#53: timed out
Server:		127.0.0.53
Address:	127.0.0.53#53

Non-authoritative answer:
Name:	google.com
Address: 142.250.66.14
Name:	google.com
Address: 2404:6800:4007:83b::200e

mtech@programming-lab-Veriton-S2690G:~$ python3 -m venv speed
(speed) mtech@programming-lab-Veriton-S2690G:~$ speedtest-cli
Retrieving speedtest.net configuration...
Testing from BSNL (117.250.233.252)...
Retrieving speedtest.net server list...
Selecting best server based on ping...
Hosted by Cherrinet - K Net Solutions Pvt Ltd (Salem) [268.27 km]: 47.391 ms
Testing download speed................................................................................
Download: 21.06 Mbit/s
Testing upload speed......................................................................................................
Upload: 3.35 Mbit/s

