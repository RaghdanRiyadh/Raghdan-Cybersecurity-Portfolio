# Security risk assessment report

## Part 1: Select up to three hardening tools and methods to implement

**1-Password hardening:** can be implemented to enforce strong password policies across the organization. Rather than relying solely on traditional methods like overly complex passwords or frequent password changes, we can follow the latest recommendations from the National Institute of Standards and Technology (NIST). These guidelines emphasize the importance of salting and hashing passwords to enhance security. By doing so, we can better protect employee credentials against unauthorized access.


**2- Firewall maintenance:** Regular firewall maintenance is crucial for maintaining a strong security posture. This involves periodically reviewing and updating security rules to ensure they are aligned with current threat landscapes. A key aspect of this is implementing port filtering by disallowing all unused ports. By doing so, we can significantly reduce the network's attack surface, limiting potential entry points for attackers and enhancing overall network security. 

**3- Multi Factor authentication (MFA):** Implementing Multi-Factor Authentication (MFA) adds an additional layer of security by requiring users to verify their identity in two or more ways before gaining access to a system or network. MFA can include various authentication methods such as passwords, PINs, badges, one-time passwords (OTP) sent to a mobile device, or biometric verification like fingerprints. This approach greatly reduces the risk of unauthorized access, even if one authentication factor is compromised.


## Part 2: Explain your recommendations


**1. Password Hardening:** I recommend implementing password hardening due to the current vulnerabilities within the organization’s password management practices. Currently, users are sharing passwords, which significantly increases the risk of brute force attacks by threat actors. If one user’s password is compromised, attackers could potentially attempt brute force attacks across all users within the organization, especially given the absence of Multi-Factor Authentication (MFA). Additionally, the database admin password is still set to its default setting, creating a significant vulnerability. If a threat actor compromises a user account, they could easily launch a brute force attack against the admin account, leading to a potential data breach. Strengthening password policies, alongside implementing MFA, will mitigate these risks and enhance the overall security of the organization.

**2. Firewall Maintenance and Enhancement:** In addition to enforcing updated security policies and rules, I recommend upgrading to a Next-Generation Firewall (NGFW) to provide an extra layer of security. NGFWs offer advanced features such as deep packet inspection and intrusion prevention, which are crucial for detecting and mitigating security threats in real-time. These firewalls can also alert administrators to potential issues, enabling faster response times. Furthermore, NGFWs are stateful, meaning they track active connections using a "state table" and only require rules in one direction. This simplifies rule management and ensures that return traffic is correctly matched to an existing session, enhancing security without adding complexity.
