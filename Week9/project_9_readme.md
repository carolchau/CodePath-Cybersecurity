Which Honeypot(s) you deployed: 
Modern Honey Network (MHN)'s Dionaea with HTTP, Conpot, Snort, Kippo as vulnerable Juniper Netscreen, p0f, elastichoney

Any issues you encountered:
Setting up using Google Cloud Platform was a little troublesome. 

A summary of the data collected: number of attacks, number of malware samples, etc.: 
- 22k+ attacks in several hours. 
- 20k+ malware samples in less than an hour. 
- Countries seen: Unknown, USA, Russia, Thailand, China, Brazil, Germany, India, Denmark, Japan, France
- TOP 5 Attacks Signatures (As of writing this post):
ET POLICY Suspicious inbound to MSSQL port 1433 (83 times)
ET DROP Dshield Block Listed Source group 1 (77 times)
ET SCAN SipCLI VOIP Scan (47 times)
ET POLICY Suspicious inbound to mySQL port 3306 (42 times)
ET CINS Active Threat Intelligence Poor Reputation IP TCP group 76 (19 times)

Any unresolved questions raised by the data collected:
Over 17k attacks were made with the same source IP of 10.128.0.2 using the TCP protocol that the suricata honeypot captures.

JSON export (called session.json) of the data collected is in this repo. 

