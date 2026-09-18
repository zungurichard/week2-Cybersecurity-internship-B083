# week2-Cybersecurity-internship-B083
Foot printing &amp;  Reconnaissance attacks with multiple Kali Tools

 🔐 Penetration Testing: Footprinting & Network Scanning

📌 Project Overview
This project was carried out as part of my practical cybersecurity and penetration testing training.
The project focused on two main areas of penetration testing:
-W2-PM1: Footprinting with Multiple Kali Linux Tools
-W2-PM5: Zenmap Based Network Scanning

The objective was to gain practical experience in reconnaissance, information gathering, DNS enumeration, web technology identification, HTTP analysis, and network discovery.
 🎯 Project Objectives
The main objectives of this project were to:
- Understand the reconnaissance stage of penetration testing.
- Gather information about an authorized target.
- Identify domain and DNS information.
- Identify technologies used by a web application.
- Analyze HTTP response headers.
- Identify possible Web Application Firewall (WAF) protection.
- Discover active hosts on an authorized network.
- Identify IP and MAC addresses where available.
- Analyze and document security-related findings.
 🛠️ Tools Used
 Tool                               Purpose
 🐉 Kali Linux : Penetration testing and cybersecurity environment 
 WHOIS :  Obtaining domain registration information 
 WhatWeb: Identifying web technologies |
 Nslookup:  Resolving domain names to IP addresses |
cURL :Analyzing HTTP response headers 
WAFW00F:  Detecting possible Web Application Firewalls 
 DNSRecon : DNS record enumeration 
Zenmap :Graphical interface for network scanning 
 Nmap :Network discovery and scanning 
 Windows CMD: Identifying local network information

 🔎 Module 1: Footprinting with Multiple Kali Tools

1. WHOIS
WHOIS was used to obtain publicly available domain registration information.

 Command
whois networkwalks.com

Information examined
   Domain Name: NETWORKWALK.COM
   Registry Domain ID: 1920256084_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.godaddy.com
   Registrar URL: http://www.godaddy.com
   Updated Date: 2026-04-13T02:24:12Z
   Creation Date: 2015-04-16T06:46:05Z
   Registry Expiry Date: 2027-04-16T06:46:05Z
   Registrar: GoDaddy.com, LLC
   Registrar IANA ID: 146
   Registrar Abuse Contact Email: abuse@godaddy.com
   Registrar Abuse Contact Phone: 480-624-2505
   Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
   Domain Status: clientRenewProhibited https://icann.org/epp#clientRenewProhibited
   Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
   Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
   Name Server: NS35.DOMAINCONTROL.COM
   Name Server: NS36.DOMAINCONTROL.COM
   DNSSEC: unsigned
   URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
>>> Last update of whois database: 2026-09-16T12:41:39Z <<<
Registrars.
Domain Name: NETWORKWALK.COM
Registry Domain ID: 1920256084_DOMAIN_COM-VRSN
Registrar WHOIS Server: whois.godaddy.com
Registrar URL: https://www.godaddy.com
Updated Date: 2026-04-12T21:24:10Z
Creation Date: 2015-04-16T01:46:05Z
Registrar Registration Expiration Date: 2027-04-16T01:46:05Z
Registrar: GoDaddy.com, LLC
Registrar IANA ID: 146
Registrar Abuse Contact Email: abuse@godaddy.com
Registrar Abuse Contact Phone: +1.4806242505
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
Domain Status: clientRenewProhibited https://icann.org/epp#clientRenewProhibited
Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
Registry Registrant ID: Not Available From Registry
Registrant Name: Registration Private
Registrant Organization: Domains By Proxy, LLC
Registrant Street: DomainsByProxy.com
Registrant Street: 100 S. Mill Ave, Suite 1600
Registrant City: Tempe
Registrant State/Province: Arizona
Registrant Postal Code: 85281
Registrant Country: US
Registrant Phone: +1.4806242599
Registrant Phone Ext:
Registrant Fax: 
Registrant Fax Ext:
Registrant Email: https://www.godaddy.com/whois/results.aspx?domain=NETWORKWALK.COM&action=contactDomainOwner
Registry Tech ID: Not Available From Registry
Tech Name: Registration Private
Tech Organization: Domains By Proxy, LLC
Tech Street: DomainsByProxy.com
Tech Street: 100 S. Mill Ave, Suite 1600
Tech City: Tempe
Tech State/Province: Arizona
Tech Postal Code: 85281
Tech Country: US
Tech Phone: +1.4806242599
Tech Phone Ext:
Tech Fax: 
Tech Fax Ext:
Tech Email: https://www.godaddy.com/whois/results.aspx?domain=NETWORKWALK.COM&action=contactDomainOwner
Name Server: NS35.DOMAINCONTROL.COM
Name Server: NS36.DOMAINCONTROL.COM
DNSSEC: unsigned
URL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/
>>> Last update of WHOIS database: 2026-09-16T12:42:00Z <<<
For more information on Whois status codes, please visit https://icann.org/epp

TERMS OF USE: The data contained in this registrar's Whois database, while believed by the
registrar to be reliable, is provided "as is" with no guarantee or warranties regarding its
accuracy.

 2. nslookup
`nslookup` was used to resolve the target domain name and identify its associated IP address.
 Command
 nslookup networkwalks.com
Information examined
Server:         192.168.128.1
Address:        192.168.128.1#53

Non-authoritative answer:
Name:   networkwalks.com
Address: 192.232.216.135

3. WhatWeb
WhatWeb was used to identify technologies exposed by the target website.
 Command
whatweb networkwalks.com

 Information examined
http://networkwalks.com [301 Moved Permanently] Apache, Cookies[__wpdm_client], Country[UNITED STATES][US], HTTPServer[Apache], HttpOnly[__wpdm_client], IP[192.232.216.135], RedirectLocation[https://networkwalks.com/], UncommonHeaders[permissions-policy,x-redirect-by,upgrade,referrer-policy,x-endurance-cache-level,x-nginx-cache]
https://networkwalks.com [200 OK] Apache, Bootstrap[7.1], Cookies[__wpdm_client], Country[UNITED STATES][US], Email[info@networkwalks.com], Frame, Google-Tag-Manager, HTML5, HTTPServer[Apache], HttpOnly[__wpdm_client], IP[192.232.216.135], JQuery[3.7.1], MetaGenerator[WordPress 7.1,WordPress Download Manager 3.3.58], Open-Graph-Protocol[website], Script[4684NR-IPIB&amp;pidnVar2=50511&amp;prtVar2=7&amp;scvVar2=12,application/json,application/ld+json,module,speculationrules,text/javascript], Title[Networkwalks Academy], UncommonHeaders[permissions-policy,link,upgrade,referrer-policy,x-endurance-cache-level,x-nginx-cache], WordPress[7.1]

 4. cURL
cURL was used to inspect HTTP response headers from the target website.
 Command
 curl -I https://networkwalks.com

 Information examined
HTTP/2 200 
permissions-policy: private-state-token-redemption=(self "https://www.google.com" "https://www.gstatic.com" "https://recaptcha.net" "https://challenges.cloudflare.com" "https://hcaptcha.com"), private-state-token-issuance=(self "https://www.google.com" "https://www.gstatic.com" "https://recaptcha.net" "https://challenges.cloudflare.com" "https://hcaptcha.com")
link: <https://networkwalks.com/wp-json/>; rel="https://api.w.org/", <https://networkwalks.com/wp-json/wp/v2/pages/53>; rel="alternate"; title="JSON"; type="application/json", <https://networkwalks.com/>; rel=shortlink
set-cookie: __wpdm_client=287b76631ba14ce0c02bb164a03965d4; path=/; domain=networkwalks.com; secure; HttpOnly
referrer-policy: no-referrer-when-downgrade
x-endurance-cache-level: 0
x-nginx-cache: WordPress
content-type: text/html; charset=UTF-8
date: Wed, 16 Sep 2026 13:10:59 GMT
server: Apache

 5. WAFW00F
WAFW00F was used to determine whether a Web Application Firewall appeared to protect the target website.
 Command
wafw00f networkwalks.com
 Purpose
The result was analyzed to determine whether WAF protection was detected.
The Web Application Firewall Fingerprinting Toolkit
    
[*] Checking https://networkwalks.com
[+] The site https://networkwalks.com is behind ModSecurity (SpiderLabs) WAF.
[~] Number of requests: 2

 6. DNSRecon
DNSRecon was used to enumerate DNS records associated with the target domain.
 Command
dnsrecon -d networkwalks.com
 DNS records examined
2026-09-16T09:17:12.649391-0400 INFO Starting enumeration for domain: networkwalks.com
2026-09-16T09:17:12.650956-0400 INFO std: Performing General Enumeration against: networkwalks.com...
2026-09-16T09:17:13.610299-0400 ERROR No answer for DNSSEC query for networkwalks.com
2026-09-16T09:17:14.339278-0400 INFO     SOA ns6135.hostgator.com 50.87.144.87
2026-09-16T09:17:15.346687-0400 INFO     NS ns6135.hostgator.com 50.87.144.87
2026-09-16T09:17:16.092465-0400 INFO     Bind Version for 50.87.144.87 "9.16.23-RH"
2026-09-16T09:17:16.093183-0400 INFO     NS ns6136.hostgator.com 192.232.216.131
2026-09-16T09:17:16.888319-0400 INFO     Bind Version for 192.232.216.131 "9.16.23-RH"
2026-09-16T09:17:18.428256-0400 INFO     MX mail.networkwalks.com 192.232.216.135
2026-09-16T09:17:18.630216-0400 INFO     A networkwalks.com 192.232.216.135
2026-09-16T09:17:20.066252-0400 INFO     TXT networkwalks.com google-site-verification=rr04eRmqHoWY3XemnizDNVK4q75X-Ij-mjgEeg-UsYI
2026-09-16T09:17:20.067127-0400 INFO     TXT networkwalks.com v=spf1 +a +mx +ip4:50.87.144.87 +include:websitewelcome.com ~all
2026-09-16T09:17:21.178298-0400 INFO Enumerating SRV Records
2026-09-16T09:17:27.037559-0400 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.9 443
2026-09-16T09:17:27.038133-0400 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.15 443
2026-09-16T09:17:27.038356-0400 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.11 443
2026-09-16T09:17:27.038547-0400 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.9 443
2026-09-16T09:17:27.039556-0400 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.11 443
2026-09-16T09:17:27.040711-0400 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.14 443
2026-09-16T09:17:27.040973-0400 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.14 443
2026-09-16T09:17:27.041971-0400 INFO     SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.15 443
2026-09-16T09:17:27.047754-0400 INFO 8 Records Found
2026-09-16T09:17:27.048890-0400 INFO Completed enumeration for domain: networkwalks.com

I also did module 4.
Foot printing and reconnaissance with theHarvester
Command
theHarvester -d microsoft.com -b Baidu

results
[*] Target: microsoft.com 

[*] Searching Baidu. 

[*] No IPs found.

[*] Emails found: 4
----------------------
,contact@microsoft.com
,support@microsoft.com
info@microsoft.com
viva-noreply@microsoft.com

[*] No people found.

[*] Hosts found: 1
---------------------
officecdn.microsoft.com


 🌐 Module 2: Zenmap Based Network Scanning
 Overview
Zenmap, the graphical interface for Nmap, was used to perform network discovery within an authorized environment.
The objective was to identify active hosts and gather basic network information.
Nmap/Zenmap was used to discover active hosts within the authorized subnet.

 Security Recommendations
1. Minimize unnecessary exposure of infrastructure information.
2. Regularly review DNS records.
3. Keep web servers, CMS platforms, frameworks and plugins updated.
4. Implement appropriate HTTP security headers.
5. Monitor devices connected to organizational networks.
6. Apply appropriate network segmentation.
7. Conduct regular authorized security assessments.
8. Properly document and remediate identified security weaknesses.

 Skills Developed
Through this project, I developed practical skills in:
  Kali Linux
  Cybersecurity
  Reconnaissance
  Network Discovery
  DNS Enumeration
  Web Technology Fingerprinting
  Network Scanning
  WAF Detection
  Security Documentation
  Nmap/Zenmap
  Linux Command Line

 Learning Outcomes
This project helped me understand that reconnaissance is an important stage of penetration testing.
I gained practical experience in collecting and analyzing information before conducting deeper security assessments. I also learned how different tools provide different pieces of information and how these results can be combined to develop an understanding of a target's exposed attack surface.
⚖️ Ethical Disclaimer
This project was conducted for educational and authorized security-testing purposes.The techniques and tools documented in this repository should only be used against systems, networks and applications where explicit permission has been obtained.
Unauthorized scanning, enumeration, exploitation, or access to computer systems may be illegal.
 👨‍💻 Author
ZUNGU RICHARD
Bachelor of Computer Science

Cybersecurity & Technology Enthusiast
⭐ Project
Penetration Testing – Footprinting & Network Scanning
Modules completed:

 W2-PM1 — Footprinting with Multiple Kali Tools
 W2-PM5 — Zenmap Based Network Scanning



