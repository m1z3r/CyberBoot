## Activity File: Find and Research Heartbleed

- In this activity, you will play the role of a penetration tester.

- You must scan your network then research and answer questions about the Heartbleed bug, which we will exploit in upcoming activities. 

You may reference the following resources and search for other information online:   
- [Common Vulnerabilities and Exposures (CVE): Heartbleed](https://cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0160)
- [US Cybersecurity and Infrastructure Security Agency (CISA): Heartbleed](https://www.us-cert.gov/ncas/alerts/TA14-098A)
- [Heartbleed.com](http://heartbleed.com/)

### Scanning

Perform the following vulnerability scans with nmap and Nessus against the Heartbleed VM
  * Nessus setup:
    - In your terminal run:   /etc/init.d/nessusd start
    - Open the Firefox browser and navigate to:   https://kali:8834
    - Clear cache in Firefox
    - Run an advanced scan against the Heartbleed VM

  * Nmap advanced vulnerability scan
    - Advanced general scan:   nmap --script=/usr/share/nmap/scripts/vulners.nse -sV `ip-address`
        * Do NOT research every vulnerability, just do a quick skim to see if you see anything that says Heartbleed or see its CVE number
    - Heartbleed specific:    nmap --script=/usr/share/nmap/scripts/ssl-heartbleed -sV `ip-address`

1. Do any of these scans find a Heartbleed vulnerability?

2. What's the primary benefit of finding a vulnerability when a scan is not specifically looking for it? (i.e. Nessus scan vs nmap specific)

3. Do your scans find any other vulnerabilities that are potentially bigger threats than Heartbleed? 


### Heartbleed Questions

Answer the following questions about Heartbleed. 

1. How does the CVE officially refer to the Heartbleed bug? 

2. Why is this vulnerability called the Heartbleed bug?

3.  Provide a brief description of the following types of  sensitive information that can be retrieved from this exploit:

    - Primary key material
    - Secondary key material
    - Protected
    - Collateral

4. What is OpenSSL? 

5. Which versions of OpenSSL are affected by this bug?

6. What are some vulnerable operating systems?

7. Find one news article about a company that was affected by the Heartbleed bug. Be prepared to share:
    - The company name.
    - The year it was attacked.
    - If provided, how many customers data were compromised because of this vulnerability.
    - Link to website article.


---
&copy; 2020 Trilogy Education Services, a 2U Inc Brand.   All Rights Reserved.

