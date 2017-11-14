Which Honeypot(s) you deployed: 
Modern Honey Network (MHN)'s Dionaea with HTTP, Conpot, Snort, Kippo as vulnerable Juniper Netscreen, p0f, elastichoney

Any issues you encountered:
Setting up using Google Cloud Platform was a little troublesome. 

A summary of the data collected: number of attacks, number of malware samples, etc.: 
- 172k+ attacks. 
- 92k+ malware samples. 
- Countries seen: Unknown, USA, Russia, Thailand, China, Brazil, Germany, India, Denmark, Japan, France, Canada, Argentina, Turkey, Chile, Great Britain
- TOP 5 Attacks Signatures (As of writing this post):
ET POLICY Suspicious inbound to MSSQL port 1433 (1,144 times)
ET POLICY Suspicious inbound to mySQL port 3306 (875 times)
ET SCAN Potential SSH Scan (457 times)
ET DROP Dshield Block Listed Source group 1 (169 times)
ET SCAN SipCLI VOIP Scan (159 times)

Any unresolved questions raised by the data collected:
There are quite a few IP addresses that made thousands of attacks, and I wonder what they are. 

A subset of the data collected (called session.json) is in this repo, as well as a gif showing you the MHN Server dashboard. 

