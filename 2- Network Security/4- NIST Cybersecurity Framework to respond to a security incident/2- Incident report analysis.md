## Summary
This morning, an intern reported to the IT department that she was unable to log in to her internal network account. However, access logs revealed that her account had been actively accessing records in the customer database, despite her being locked out. The intern mentioned that she received an email this morning instructing her to visit an external website and log in with her internal network credentials to retrieve a message. We believe this was the method used by a malicious actor to gain unauthorized access to our network and customer database. Additionally, several employees have reported that customer records are either missing or contain incorrect data. It appears that customer data was not only exposed to the attacker but also deleted or manipulated.

### Identify
We have determined that the firewall was compromised by an ICMP flood attack, leading to a disruption in the internal network. As a result, all users were unable to log in to their internal network accounts, causing a business continuity interruption for approximately two hours until the cybersecurity team mitigated the threat. Additionally, the customer database was either deleted or manipulated during the attack. 


### Protect: 
To address the vulnerabilities and prevent future incidents, we have implemented the following measures:
- Firewall Policies and Rules: We have updated the firewall to limit the rate of incoming ICMP packets and ensure regular firewall maintenance procedures are in place.
- Least Privilege Principle: We have enforced the principle of least privilege to minimize the risk of unauthorized access.
- Multi-Factor Authentication (MFA): MFA has been implemented to add an additional layer of security for internal network logins.
- Employee Training: All employees, including interns, will undergo training on protecting their login credentials.
- Database Hardening: We have updated procedures for data encryption and restricted access to sensitive areas of the database.
- Intrusion Prevention System (IPS): An IPS has been implemented to protect against potential future attacks.

###  Detect
We have deployed IPS and enhanced firewall logging tools to monitor and detect any unauthorized access attempts and incoming traffic from the internet. This will enable us to identify and respond to threats more effectively in the future.

### Respond
To contain the threat, all intern network accounts have been temporarily disabled to prevent further brute force attacks. We are also providing additional training to all interns and employees on how to safeguard their login credentials. In compliance with legal and regulatory requirements, we have informed our management team about the data breach, and they will initiate the process of notifying customers and clients. Management will also notify law enforcement and other relevant organizations as required by local laws.
inform law enforcement and other organizations as required by local laws.


### Recover
Fortunately, we had a full backup from the previous night, which will allow us to restore the deleted or manipulated database. However, any data entered or modified since the last backup will not be recorded. Therefore, we will request customers to re-enter their information once the database has been fully restored.
Increase Backup Frequency :Implement more frequent backups (e.g., hourly) to reduce data loss between backups.
Data Redundancy and Replication: Use data replication and RAID configurations to ensure data availability and protection against hardware failures.



## Reflections/Notes: 
This incident highlights the importance of robust cybersecurity practices, including employee training, strict access controls, and regular system backups. Moving forward, we will continue to enhance our security measures and response strategies to better protect our network and customer data from future threats.

