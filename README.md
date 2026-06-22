# Networking-Lab-Static-Routing

Static routing is a manual way to tell a router which next hop to use to reach a remote network, the usual goal is to configure routes between LANs so devices can ping each other across routers.
This lab demonstrates how to manually configure router paths so different subnets can communicate without dynamic routing.

Router

1. Access Router:
2. 
•	Enter privileged EXEC mode (to run advanced commands):

enable

•	Enter global configuration mode (to make configuration changes):

configure terminal

2. Configure Interface IP Address:
3. 
•	Enter interface configuration mode :

	interface Ethernet0/0

•	Set IP address and subnet mask:
	ip address 135.126.4.1 255.255.255.252

•	Enable the interface (if it’s administratively down):

no shutdown

Configure all the router interface in similar way.

3. Save Configuration:
4. 
•	Save the current configuration to startup-config (to retain changes after reboot):

	write 
Or:
copy running-config startup-config

6. Exit Router Mode:
   
•	Exit to previous mode:

exit
Or:
Cltr z

Static routing command:

	ip route 135.126.0.0 255.255.254.0 135.126.4.6
	ip route 135.126.2.0 255.255.255.0 135.126.4.
(Include all the ip address that is not directly connected)
Configure all the router interface in similar way.

Router

 Configure PC IP address:
 
	ip 135.126.3.2/24 135.126.3.1
	save

•	Check PC IP address:

	Show ip
	
•	Configure all the pc’s interface in similar way.

Ping test result:
 

Trace route result:
 






**
