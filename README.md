# Assessment 02 - Networking

This contains a list of questions to assess a fellows knowledge of the **Networking** Learning Outcome

## Questions

1. Display network interfaces

	```
	'ip link' or 'ifconfig'
	```

2. Display network routing table

	```
	'ip route' or 'route'
	```

3. Disable **ICMP** ping requests to your local machine

	```
	sudo bash -c 'echo 1 > /proc/sys/net/ipv4/icmp_echo_ignore_all'
	```

4. Use a subnet mask to allocate IP addresses on a network

	Given the ip range **10.0.10.0/24**

	```
	minimum_ip_address="<10.0.10.1>"
	maximum_ip_address="<10.0.10.254>"
	```

	Given the ip range **10.0.10.0/30**

	```
	minimum_ip_address="<10.0.10.1>"
	maximum_ip_address="<10.0.10.2>"
	```

5. Use `ssh` to forward port **2444** on remote machine **10.0.0.1** to local port **6333**

	```
	ssh -L 6333:10.0.0.1:2444 localhost
	```

6. Using `ssh` with authentication agent forwarded, connect to remote machine **10.0.0.1**

	```
	ssh -A user@10.0.0.1
	```

7. Using `ssh`, connect to remote machine **10.0.0.1** with the private key `private.key.pem`

	```
	ssh -i 'private.key.pem' user@10.0.0.1
	```

8. Using `scp`, copy file `/home/user/file.txt` on remote machine **10.0.0.1** to your local machine

	```
	scp user@10.0.0.1:/home/user/file.txt .
	```

9. Using `scp`, copy local file at `/home/user/file.txt` to remote machine **10.0.0.1**

	```
	scp /home/user/file.txt user@10.0.0.1:/home/user
	```

10. List all open ports on a system

	```
	netstat -lntu
	```

11. Block ip address from accessing all ports on your local machine using iptables

	```
	iptables -A INPUT -s <ip address> -p 0 -j DROP
	```

12. List differences between IPV4 & IPV6 addresses

	```
	IPv4 uses 32 bits (4 bytes) address scheme while IPv6 uses a 128-bit (16 bytes) address scheme
	```

	```
	Packet size:	For IPv4, 576 bytes is required and fragmentation is optional while for IPv6 1280 bytes is required without fragmentation
	```

	```
	NAT: (IPv4) Yes (IPv6) No
	```
	