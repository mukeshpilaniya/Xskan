#XSKAN

XSKAN - Cross-Site Scripting Scanner

Author: [Mukesh Pilaniya](http://www.99hacking.com)

Disclaimer: I am not responsible for any damage done using this tool. This tool should only be used for educational purposes and for penetration testing.


###Compatibility: 
* Windows , Linux or any device running python 2.7

###Requirements: 

* Python 2.7

* Wordlist included(wordlist.txt)

* Modules required: Colorama, Mechanize


###Modules Required:

* Colorama:  https://pypi.python.org/pypi/colorama/

* Mechanize: https://pypi.python.org/pypi/mechanize/


###Description:
**XSKAN** is a very powerful and fast Cross-Site Scripting Scanner which is used for bruteforcing a parameters. The Xskan injects multiple payloads loaded from a specified wordlist and fires them at the specified parameters and scans if any of the parameter is vulnerable to XSS vulnerability. Xskan is very accurate at doing its task and there is no chance of false positive as the scanning is much powerful. Xskan supports POST and GET requests which makes it compatible with the modern web applications.

###Features:

* XSS Bruteforcing

* XSS Scanning

* Supports GET/POST requests

* Custom wordlist can be included

* User-friendly UI

###Usage(GET Method):

```
COMMAND:  python xskan.py
METHOD:   g
URL:      http://www.site.com/?parameter=value
WORDLIST: wordlist.txt
```

###Usage(POST method):

```
COMMAND:   python xskan.py
METHOD:    p
URL:       http://www.site.com/file.php
POST DATA: parameter=value&parameter1=value1
WORDLIST:  wordlist.txt
```

###Output:

```
  
             . -
            o   \     .-. 
               .----.'   \ 
             .'o)  / `.   o 
            /         | 
            \_)       /-. 
              '_.`    \  \ 
               `.      |  \ 
                |       \ | 
            .--/`-.     / / 
          .'.-/`-. `.  .\| 
         /.' /`._ `-    '-. 
    ____(|__/`-..`-   '-._ \ 
   |`------.'-._ `      ||\ \ 
   || #   /-.   `   /   || \| 
   ||   #/   `--'  /  /_::_|)__ 
   `|____|-._.-`  /  ||`--------` 
         \-.___.` | / || #      | 
          \       | | ||   #  # | 
          /`.___.'\ |.`|________| 
          | /`.__.'|'.` 
        __/ \    __/ \ 
       /__.-.)  /__.-.) 
 __  __  ____    _  __     _      _   _ 
 \ \/ / / ___|  | |/ /    / \    | \ | |
  \  /  \___ \  | ' /    / _ \   |  \| |
  /  \   ___) | | . \   / ___ \  | |\  |
 /_/\_\ |____/  |_|\_\ /_/   \_\ |_| \_|

                                            
 xskan - Cross-Site Scripting Scanner
 
 Author: Mukesh Pilaniya - http://99hacking.com


Select method: [G]ET or [P]OST (G/P): p
[?] Enter URL:
[?] > http://site.com/file.php
[+] Checking if site.com is available...
[+] site.com is available! Good!
[?] Enter post data: > parameter=value&parameter1=value1
[?] Enter location of Wordlist (Press Enter to use default wordlist.txt)
[?] > wordlist.txt
[+] Using Default wordlist...
[+] Loading Payloads from specified wordlist...
[+] 25 Payloads loaded...
[+] Injecting Payloads...

[+] Testing 'parameter' parameter...
[+] 2 / 25 payloads injected...
[!] XSS Vulnerability Found! 
[!] Parameter:	parameter
[!] Payload:	"><script>prompt(1)</script>

[+] Testing 'parameter1' parameter...
[+] 25 / 25 payloads injected...
[+] 'parameter1' parameter not vulnerable.
[+] 1 Parameter is vulnerable to XSS.
+----+--------------+----------------+
| Id | Parameters   |     Status     |
+----+--------------+----------------+
| 0  |  parameter   |  Vulnerable    |
+----+--------------+----------------+
| 1  |   parameter1 | Not Vulnerable |
+----+--------------+----------------+

```
