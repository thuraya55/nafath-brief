Version: NAFATH-V4
Track: Networking

## Overview
A national service provider depends on a chain of software, data, infrastructure and external services, so a weakness in one component can affect the whole service. Configuration and secrets must be managed separately from source code, while a Software Bill of Materials helps identify third-party components and their known risks. AI systems also need testing against attacks that manipulate inputs, training data or model behavior. Mobile applications should be checked against a recognized security standard to protect stored information, authentication and network traffic. Network operators must validate routing information and understand the limits of those controls. Vulnerability management is equally important: severe flaws in widely used libraries can expose connected systems, making timely patching and inventory essential. This brief examines BGP route hijacking and how RPKI helps limit unauthorized route announcements.
## Software
The Twelve-Factor App recommends storing configuration separately from code. Secrets such as passwords and API keys should not be committed to a repository. Instead, use environment variables or a secure secrets manager, restrict access, and rotate exposed credentials. This reduces the risk of leaking sensitive information when code is shared or deployed.
Resource: The Twelve-Factor App - Config - https://12factor.net/config
## AI
Adversarial attacks can target AI systems in different ways. Evasion attacks manipulate inputs at inference time to cause incorrect predictions. Poisoning attacks corrupt training data or the training process so the model learns harmful behavior. Defenses include validating data, monitoring model performance, testing with adversarial examples, and controlling access to training pipelines.
Resource: NIST - Adversarial Machine Learning - https://www.nist.gov/itl/ai-risk-management-framework
## Mobile
The OWASP Mobile Application Security Verification Standard (MASVS) provides security requirements for mobile applications. It covers areas such as secure storage, cryptography, authentication, network communication, and platform interaction. Developers can use MASVS to guide security testing and identify weaknesses before release. Following a standard helps structure testing, but does not guarantee that an application is completely secure.
Resource: OWASP - MASVS - https://mas.owasp.org/MASVS/
## Networking
BGP hijacking occurs when an autonomous system announces IP prefixes it is not authorized to originate, potentially redirecting or disrupting internet traffic. Resource Public Key Infrastructure (RPKI) helps operators validate route-origin authorization records through Route Origin Validation (ROV). However, RPKI does not prevent every routing attack: it mainly checks whether the origin AS is authorized for a prefix, not the entire AS path. Operators should combine RPKI with monitoring and sound routing policies.
Resource: RIPE NCC - RPKI - https://www.ripe.net/manage-ips-and-asns/resource-management/rpki/
## Cybersecurity
Log4Shell is a critical remote code execution vulnerability in Apache Log4j 2, tracked as CVE-2021-44228. An attacker may exploit vulnerable applications by sending specially crafted input that triggers unsafe lookup behavior. Organizations should identify affected Log4j versions, upgrade to a fixed version recommended by Apache, and check for signs of exploitation. Disabling vulnerable functionality alone may not be a reliable substitute for applying the appropriate security updates.
Resource: Apache Logging Services - Log4j Security Vulnerabilities - https://logging.apache.org/log4j/2.x/security.html
## Data
A Software Bill of Materials (SBOM) is a formal inventory of software components and dependencies. It helps organizations understand what is included in an application and respond faster when a component has a known vulnerability. An SBOM should include the supplier, component name, version, unique identifiers where available, dependency relationships, and information about the SBOM author and creation time. It should be maintained as software changes and kept accurate.
Resource: CISA - Software Bill of Materials (SBOM) - https://www.cisa.gov/sbom
## Misconception in My Track
A common misconception is that enabling RPKI completely prevents BGP hijacking. In reality, RPKI Route Origin Validation (ROV) checks whether the originating autonomous system is authorized to announce a prefix, but it does not validate the entire AS path. Therefore, some routing attacks can still occur even when RPKI is deployed. Network operators should combine RPKI with route monitoring and other routing security practices. RPKI improves routing security, but it is not a complete solution. The RIPE NCC guidance on RPKI and Route Origin Validation explains the scope and limitations of origin validation.
Resource: RIPE NCC - RPKI - https://www.ripe.net/manage-ips-and-asns/resource-management/rpki/
## Open Question 
How can national service providers encourage wider RPKI adoption while detecting routing attacks that RPKI origin validation cannot identify?
