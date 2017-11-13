# Project 8 - Pentesting Live Targets

Time spent: **5** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: Session Hijacking/Fixation
	- A browser where the user was not logged in can get logged-in privileges by changing its session so that it is equal to the value of PHPSESSIONID from a browser where the user is logged in.
	(https://github.com/carolchau/CodePath-Cybersecurity/blob/master/Week8/gifs/blue1.gif)
	
Vulnerability #2: SQL Injection (SQLi)
	- Setting the id URL parameter to ' OR SLEEP(3)=0--' causes the server to sleep. 
	(https://github.com/carolchau/CodePath-Cybersecurity/blob/master/Week8/gifs/blue2.gif)


## Green

Vulnerability #1: Username Enumeration
	- Putting a correct username in the login form will yield a bolded error message. However, if done with an incorrect username, the error message is not bolded. 
	(https://github.com/carolchau/CodePath-Cybersecurity/blob/master/Week8/gifs/green1.gif)

Vulnerability #2: Cross-Site Scripting (XSS)
	- JavaScript that is left as a comment will execute when a logged-in user checks the feedback page. 
	(https://github.com/carolchau/CodePath-Cybersecurity/blob/master/Week8/gifs/green2.gif)


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
	- Changing the value of the id parameter will enable a user to see sensitive information about certain salespeople. Spoilers: One was fired for stealing and the other was not supoosed to be public until September 1st.)
	(https://github.com/carolchau/CodePath-Cybersecurity/blob/master/Week8/gifs/red1.gif)

Vulnerability #2: Cross-Site Request Forgery (CSRF)
	- Using Burp Suite to send a POST request of the "edit_salesperson" form to edit saleperson information. An attacker can create a hidden form to send the same POST request. 
	(https://github.com/carolchau/CodePath-Cybersecurity/blob/master/Week8/gifs/red2.gif)

