## Solution Guide: Researching Heartbleed
The goal of this activity was to gather background information on the Heartbleed vulnerability.

---

### Scanning

1. Do any of these scans find a Heartbleed vulnerability?
    - Nessus finds Heartbleed
    - Nmap's vulners script does not find Heartbleed
    - Nmap's heartbleed specific script shows the VM is vulnerable to Heartbleed

2. What's the primary benefit of finding a vulnerability when a scan is not specifically looking for it? (i.e. Nessus scan vs nmap specific)
    - It is significantly easier to find a known vulnerability when you scan for it directly. The primary benefit of a general scan is finding vulnerabilities you are not aware of. What if you didn't know your system was vulnerable to Heartbleed and didn't think to look for it? In this example, the Nessus scan was able to detect it.
    - However, it is good to take note about vulnerability scanning from Offensive Security: "When used properly, this is a great asset to a pen tester, yet it is not without it’s draw backs. Vulnerability scanning is well known for a high false positive and false negative rate. This has to be kept in mind when working with any vulnerability scanning software."

3. Do your scans find any other vulnerabilities that are potentially bigger threats than Heartbleed? 
    - The Nessus scan shows SSL vulnerabilities with higher CVSS than Heartbleed
    - Nmap's vulners script shows numerous vulnerabilities with higher CVSS

### Heartbleed Questions

Answer the following questions about Heartbleed. 

1. How does the CVE officially refer to the Heartbleed bug? 
    - This bug is officially referred to as CVE-2014-0160.

2. Why is this vulnerability called the Heartbleed bug?

   - There is a bug in OpenSSL's Heartbeat extension. When exploited, it leaks ("bleeds") memory content from the server to the attacker and the attacker to the server.

3.  Provide a brief description of the following types of sensitive information that can be retrieved from this exploit:

      - Primary key material: Encryption keys, which are the prime target. These leaked secret keys allow the attacker to decrypt any traffic to the protected services and to impersonate the service at will.

      - Secondary key material: Data such as user credentials.

      - Protected: The data that is handled by the company that was attacked. This could include, for example, medical records and credit cards.

      - Collateral: Other details that have been exposed to the attacker in the leaked memory content. This may contain technical details such as memory addresses, and security measures such as canaries used to protect against overflow attacks.

4. What is OpenSSL? 

   - OpenSSL provides cryptographic services such as SSL/TLS to the applications and services.

5. Which versions of OpenSSL are affected by this bug?
  
   - OpenSSL 1.0.1 through 1.0.1f.

6. What are some vulnerable operating systems?

    - Debian Wheezy (stable) - OpenSSL 1.0.1e-2+deb7u4
    - Ubuntu 12.04.4 LTS - OpenSSL 1.0.1-4ubuntu5.11
    - CentOS 6.5 - OpenSSL 1.0.1e-15
    - Fedora 18 - OpenSSL 1.0.1e-4
    - OpenBSD 5.3 - OpenSSL 1.0.1c 10 May 2012; OpenBSD 5.4 - OpenSSL 1.0.1c 10 May 2012
    - FreeBSD 10.0 - OpenSSL 1.0.1e 11 Feb 2013
    - NetBSD 5.0.2 - OpenSSL 1.0.1e
    - OpenSUSE 12.2 - OpenSSL 1.0.1c

7. Find one news article about a company that was affected by the Heartbleed vulnerability. Be prepared to share:
    
    - The company name: Community Health Systems
    - The year it was attacked: 2014
    - If provided, how many customers data were compromised because of this vulnerability: 4.5 million patients
    - Link to website article: https://time.com/3148773/report-devastating-heartbleed-flaw-was-used-in-hospital-hack/


---
&copy; 2020 Trilogy Education Services, a 2U Inc Brand.   All Rights Reserved.

