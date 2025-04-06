### BloodHound and Cobalt Strike DNS Detector
A lightweight and simple DNS analysis tool written in Spicy for detecting common Active Directory reconnaissance activities and C2 communications.
```version
spicy-driver version: spicy-driver v1.12.0 (0e1959ac)
```
Overview
This tool analyzes DNS query logs to identify suspicious patterns associated with:

BloodHound - Active Directory reconnaissance and mapping tool
Cobalt Strike - Red team C2 framework with DNS-based communication features
KDC Enumeration - Attempts to discover and enumerate Kerberos infrastructure
Key Features
Fast, efficient parsing of DNS logs using Spicy's high-performance capabilities
Pattern-based detection of common Active Directory enumeration techniques
Simple output with clear indicators of which tool/technique was detected
Lightweight implementation with minimal dependencies
Detection Methods
The tool identifies suspicious DNS activity by recognizing patterns such as:

Service discovery queries for domain controllers, LDAP, and Kerberos services
Computer account enumeration patterns
Abnormally long domain names typical of encoded C2 traffic
Specific subdomains and record types associated with red team tools
```Usage
cat dns_logs.txt | spicy-driver -p DNSAnalyzer::DNSLog bloodHound_cobaltstrike_KDC_Enum.spicy
```
Perfect for blue teams looking to monitor Active Directory environments for reconnaissance activities and potential command-and-control channels.
