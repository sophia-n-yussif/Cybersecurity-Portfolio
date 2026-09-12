Exercise Context

Source
Traffic Analysis Exercise, malware-traffic-analysis.net, 2026-01-31
https://www.malware-traffic-analysis.net/2026/01/31/index.html

Environment
Organization: Win11Office (fictional, provided by exercise)
Domain: win11office.com
Active Directory environment name: WIN11OFFICE
Domain Controller: 10.1.21.2 - WIN-LU4L24X3UB7
LAN segment: 10.1.21.0/24 (10.1.21.0 through 10.1.21.255)
LAN segment gateway: 10.1.21.1
LAN segment broadcast address: 10.1.21.255

Background
As an analyst at a Security Operations Center, I reviewed alerts from the past week and found a signature hit for ET MALWARE Lumma Stealer Victim Fingerprinting Activity. The alert triggered on traffic from 153.92.1.49 over TCP port 80, on 2026-01-27 at 23:05 UTC. Using this alert, I retrieved a packet capture of the traffic from the internal IP address that triggered it, in order to identify the affected host and user and write up an incident report for the response team.

Investigative Questions
- What is the IP address of the infected Windows client?
- What is the MAC address of the infected Windows client?
- What is the host name of the infected Windows client?
- What is the user account name from the infected Windows client?
- What is the full name of the user from the user account?
- What is the domain from 153.92.1.49 that triggered the alert for Lumma Stealer?

Tools Used
Wireshark 4.6.7 (x64)
