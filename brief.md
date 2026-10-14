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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question 
