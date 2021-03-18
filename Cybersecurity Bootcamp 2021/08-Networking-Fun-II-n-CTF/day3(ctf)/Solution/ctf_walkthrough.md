# How to find the flags for the PCAP files and the bonus question

# CTF 1
12. How many total Packets in the pcap file
    - Number listed on the bottom right of Wireshark window
13. How many ARP Packets?
    - Filter for "arp"
    - Total number on bottom right of Wireshark window
14. What domain did the user first try to access?
    - Filter for "dns"
    - Click on packet #15
    - The website/domain is listed in the "info" column
    - Also located in Packet Details > Domain Name System
15. What HTTP response code did the user get?
    - Filter for "http"
    - Packet #24 "info" column contains response code
    - Also located in Packet Details > Hypertext Transfer Protocol
16. What primary domain was the website directed to?
    - Filter for "http"
    - Packet #24
    - Located under Packet Details > Hypertext Transfer Protocol > "Location"
17. What is the status code of packet number 36?
    - Click on packet #36
    - Status code located in "info" column
    - Also located under Packet Details > Hypertext Transfer Protocol
18. What is the source port of original HTTP request?
    - Filter for "http"
    - Packet #23 is the original HTTP request
    - Source port is located under Packet Details > Transmission Control Protocol
19. What is the primary NS server of the website being requested?
    - Filter for "dns"
    - Click on packet #20 (first "AAAA" response)
    - NS server located in "info" column after SOA (Start of Authority record)
    - Also located in Packet Details > Domain Name System > Answers
20. What is the TTL of the A record of the original website requested?
    - Filter for "dns.resp.ttl"
    - Packet #19
    - TTL located in Packet Details > Domain Name System > Answers > "Time to live"
21. In the one SYN/ACK packet, what is the time between this and the previous SYN packet in seconds? (use exact value provided in the packet)
    - Filter for "tcp.flags.syn == 1"
    - Subtract time of packet #25 from packet #26
22. What is Homer Simpson's phone number (with dashses)
    - Filter for "frame contains homer"
    - Right click on packet #46 > Follow > TCP stream
    - Plain text reveals information
    - Also located in Packet Bytes
23. Where does Homer want Marge to meet him?
    - Filter for "frame contains homer"
    - Right click on packet #46 > Follow > TCP stream
    - Plain text reveals information
24. What is the vendor name of Homer's NIC? (five letters)
   - Filter for "frame contains homer"
   - Click on packet #46
   - Located in Packet Details > Ethernet II

# CTF 2
50. Decrypt the wireless PCAP with the WPA key. How many HTTP packets?
    - Click on Edit > Preferences > Protocols > IEEE 802.11
    - Check the box to "Enable decryption"
    - Click "Edit" by Decryption keys
    - Select "wpa-wd" under Key type and type "Induction" under Key
    - Click "apply" or "okay" as needed to go back to the packet capture
    - Filter for "http"
    - Answer located on bottom right of Wireshark window
51. IP address of Karens-imac.local
    - Filter for "http"
    - Click on packet #439
    - IP located in Packet Details under Internet Protocol Version 4
52. IP address of rr.pmtpa.wikimedia.org
    - Filter for "http"
    - Click on packet #439
    - IP located in Packet Details under Internet Protocol Version  
53. What is the SSID of the wireless router?
    - Click on the Wireless menu > WLAN traffic
    - Answer located in SSID column
54. DNS provides this TTL for the CNAME of en-wikimedia.org
    - Filter
55. Total count of SUCCESSFUL ICPM, "DESTINATION REACHABLE" packets
    - Filter for "icmp.type==0"
    - No packets show up
56. Television show the user was viewing the transcripts for (three letters)
    - Filter for "http"
    - Several destination addresses contain the word "transcript"

# CTF 3
57. What is the primary protocol in these packets?
    - Visible when opening packet in the "protocol" column
58. What is the likely true MAC address of 192.168.1.254
    - Click on packet #2
    - In Packet Details it shows "Duplicate IP" detections
    - The most likely MAC is the first one it detected after the first "also in use by"
59. Which is likely the hacker's MAC address of 192.168.1.254
    - Based off the previous question, the other MAC addresses that appear in the first IP conflict would be the potential hacker's
60. What year did this traffic occur?
    - The date can be found in Packet Details > Frame > "Arrival Time"

# Bonus
61. For a network with 352 devices, how many connections would you need for a fully connected network?
    - The formula is: "n(n-1 /2)"
    - Answer: 352(352-1) / 2 = 61766
62. How many usable hosts are in 66.56.54.194/19?
    - The formula is: "2^(broadcast - network address)-2"
    - Answer: 2 ^ (32-19) - 2 = 8190
63. What is the complete in-addr.arpa for the above IP (before the in-addr.arpa)?
    - For the ARPA, take the IP and switch the order of the octets from last to first. 66.56.54.194 becomes the ARPA IP of 194.54.56.66
64. For 2001:db8:85a3::8a2e:370:7334 and prefix length 107, what is the total number of hosts?
    - Using an IPv6 CIDR calculator, enter the IPV6 value with the CIDR notation, 2001:db8:85a3::8a2e:370:7334/107, and it returns the number of hosts: 2097152

