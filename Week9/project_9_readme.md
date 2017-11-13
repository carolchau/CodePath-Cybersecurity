Which Honeypot(s) you deployed: 
Modern Honey Network (MHN)'s Dionaea with HTTP, Conpot, Snort, Kippo as vulnerable Juniper Netscreen, p0f, elastichoney

Any issues you encountered:
Setting up using Google Cloud Platform was a little troublesome. 

A summary of the data collected: number of attacks, number of malware samples, etc.: 
- 3,000+ attacks in less than an hour. 
- 30+ malware samples in less than an hour. 
- Countries seen: Unknown, USA, Russia, Thailand, China, Brazil, Germany, India, Denmark, Japan
- TOP 5 Attacks Signatures (As of writing this post):
ET POLICY Suspicious inbound to MSSQL port 1433 (9 times)
ET DROP Dshield Block Listed Source group 1 (4 times)
ET POLICY Suspicious inbound to Oracle SQL port 1521 (2 times)
ET POLICY Suspicious inbound to mySQL port 3306 (2 times)
ET CINS Active Threat Intelligence Poor Reputation IP TCP group 58 (1 times)

Any unresolved questions raised by the data collected:
There are a lot of repeated attacks. One of which is done with the source IP of 10.128.0.2 using the TCP protocol that suricata honeypot captures. 

JSON export (called session.json) of the data collected is in this repo. 

