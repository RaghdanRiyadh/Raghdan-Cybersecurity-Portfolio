## Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log.


**1- The UDP protocol reveals that:** 53

**2- This is based on the results of the network analysis, which show that the ICMP echo reply returned the error message:** The ICMP echo reply returned the error message "Destination Port Unreachable." This indicates that the network or host receiving the ICMP packet was unable to communicate with the intended service on UDP port 53, which is typically used for DNS.

**3- The port noted in the error message is used for:** The port noted in the error message, UDP port 53, is used for DNS (Domain Name System) services. This port handles requests for resolving domain names to IP addresses. 

**4- The most likely issue is:** The most likely issue is a problem with the DNS service, potentially caused by a DoS/DDoS attack, a firewall misconfiguration blocking UDP port 53, or a DNS server outage or misconfiguration, leading to the "Destination Port Unreachable" error



## Part 2: Explain your analysis of the data and provide at least one cause of the incident.

**1- Time incident occurred:** 13:24:32

**2- Explain how the IT team became aware of the incident:** The IT team was alerted to the incident when several customers reported being unable to access the client's website, www.yummyrecipesforme.com. The error message displayed was "Destination Port Unreachable."

**3- Explain the actions taken by the IT department to investigate the incident:** 
To investigate the issue, Cyber Security analysts attempted to load the webpage while running a network analysis using the tool Tcpdump. The logs revealed an error indicating that UDP port 53 was unreachable. The logs also showed a flag with "+A," identifying the issue as related to the DNS (Domain Name System) service, specifically the A record, which maps domain names to IP addresses. Based on this information, the team continued to investigate further to determine the root cause of the website's inaccessibility. 

**4- Note key findings of the IT department's investigation (i.e., details related to the port affected, DNS server, etc.):** The affected port was UDP port 53, which is critical for DNS services. The inability to reach this port suggests a disruption in DNS resolution, preventing users from accessing the website.

**5- Note a likely cause of the incident:** 

**1. Denial of Service (DoS) or Distributed Denial of Service (DDoS) Attack:**
A potential cause could be a DoS or DDoS attack, where a threat actor may have launched an ICMP flood or a "Ping of Death" attack. Such attacks overwhelm the server's bandwidth, leading to server crashes and the subsequent "Destination Port Unreachable" error.

**2. Firewall Misconfiguration:**
The incident could have been caused by an accidental firewall misconfiguration, where a security engineer might have unintentionally blocked UDP port 53. This blockage would prevent DNS queries from reaching the server, leading to the reported error.

**3. DNS Server Configuration Issues:**
Another possible cause could be a misconfiguration or outage on the DNS server itself. If the DNS server was down or improperly configured, it would be unable to respond to queries, resulting in the error observed.