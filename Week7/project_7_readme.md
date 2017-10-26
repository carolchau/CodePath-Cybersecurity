# Project 7 - WordPress Pentesting

Time spent: 3 hours spent in total

> Objective: Find, analyze, recreate, and document at least 3 exploits affecting an old version of WordPress

## Pentesting Report

1. WordPress <= 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: Cross-Site Scripting (XSS)
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: ![Exploit 1](https://github.com/carolchau/CodePath/Week7/gifs/w7exploit1.gif)
  - [ ] Steps to recreate: 
  	- Create a new post
	- Enter HTML containing Javascript.  
  - [ ] Affected source code:
    - [CVE-2015-5622](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5622)
	- [CVE-2015-5623](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5623)
2. WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: Cross-Site Scripting (XSS)
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: ![Exploit 2](https://github.com/carolchau/CodePath/Week7/gifs/w7exploit2.gif) 
  - [ ] Steps to recreate: 
  	- Comment on a post (no authentication needed)
	- Enter HTML containing Javascript that is over 64kb long.
  - [ ] Affected source code:
    - [wpvulndb](https://wpvulndb.com/vulnerabilities/7945)
3. WordPress Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: Cross-Site Scripting (XSS)
    - Tested in version: 4.2
    - Fixed in version: 4.6
  - [ ] GIF Walkthrough: ![Exploit 3](https://github.com/carolchau/CodePath/Week7/gifs/w7exploit3.gif) 
  - [ ] Steps to recreate: 
  	- Comment on a post (no authenticaton needed)
	- Enter Javascript code
  - [ ] Affected source code:
    - [GitHub](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)
	
## Assets

WordPress <= 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS):
```
<a href="[caption code=">]</a><a title=" onmouseover=alert('test')  ">link</a>
```
https://klikki.fi/adv/wordpress3.html


WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS): 
```
<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>
```
http://klikki.fi/adv/wordpress2.html


## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [GIPHY Capture](https://giphy.com/apps/giphycapture).

## Notes

Had some issues setting up wpdistillery, but after it was set up, doing the exploits were pretty straightforward. 

## License

    Copyright 2017 Carol Chau

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
