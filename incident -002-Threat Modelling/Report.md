## Executive Summary
Threat modelling is a systematic approach to identifying, prioritising, and addressing potential security threats across the organisation. By simulating possible attack scenarios and assessing the existing vulnerabilities of the organisation's interconnected systems and applications, threat modelling enables organisations to develop proactive security measures and make informed decisions about resource allocation. Threat modelling can be done with different frameworks such as the Mitre ATT&CK framework, DREAD framework, STRIDE framework and the PASTA framework.

## Objective
Threat modelling aims to reduce an organisation's overall risk exposure by identifying vulnerabilities and potential attack vectors, allowing for adequate security controls and strategies. This process is essential for constructing a robust defence strategy against the ever-evolving cyber threat landscape.

## Scenario
A financial technology company was preparing to launch a new online banking platform that would allow customers to transfer funds, pay bills, and manage accounts through a web application and mobile app.

Before deployment, the security team conducted a threat modeling exercise to identify potential risks. They mapped the system architecture, including users, application servers, databases, and third-party payment gateways. During the exercise, they identified several threats, such as credential theft through phishing, unauthorized access due to weak authentication, interception of sensitive data during transmission, and abuse of exposed APIs.

As a result of the threat modeling process, the company implemented multi-factor authentication (MFA), encrypted all sensitive communications, and added monitoring for suspicious account activities. By addressing these risks before launch, the organization reduced the likelihood of security incidents and improved the overall security posture of the banking platform.

## Tools USed 
* MITRE ATT&CK Framework – Used to map adversary tactics, techniques, and procedures (TTPs) to potential attack scenarios.
* MITRE ATT&CK Navigator – Used to visualize and analyze ATT&CK techniques relevant to the system being assessed.
* STRIDE Framework – Used to identify and categorize security threats affecting the application.
* DREAD Framework – Used to evaluate and prioritize identified threats based on their potential impact and likelihood.
* PASTA Framework – Used to perform a risk-centric analysis by considering business objectives, technical assets, and potential attack paths.
* TryHackMe Lab Environment – Used to reinforce the practical concepts of threat modelling.
  
## Threat Profile
The threat modelling exercise identified multiple threats that could affect the online banking platform. The primary threats included phishing attacks targeting customer credentials, unauthorized access resulting from weak authentication mechanisms, interception of sensitive information during data transmission, and exploitation of exposed application programming interfaces (APIs).

Potential threat actors included cybercriminals seeking financial gain, insider threats with unauthorized access to sensitive systems, and organized threat groups capable of conducting targeted attacks against financial institutions.

## MITRE ATT&CK Mapping
The identified threats were mapped to the MITRE ATT&CK framework to better understand adversary behaviour and support defensive planning.

Relevant Tactics

* Initial Access (TA0001)
* Credential Access (TA0006)
* Discovery (TA0007)
* Collection (TA0009)
* Exfiltration (TA0010)
* Command and Control (TA0011)

The MITRE ATT&CK Navigator was used to visualize the relevant tactics and techniques, enabling the security team to prioritize defensive measures and improve detection capabilities.

## Investigation Analysis
The threat modelling assessment began by defining the scope of the online banking platform and identifying critical assets, including customer accounts, transaction records, authentication services, and payment processing systems.

Potential threats were then identified using structured threat modelling methodologies. The STRIDE framework was applied to categorize possible threats, while the DREAD framework was used to evaluate and prioritize risks based on their potential impact. The PASTA framework provided additional context by aligning identified threats with business objectives and likely attack scenarios.

Following the assessment, appropriate security controls were recommended to reduce the identified risks. These included implementing multi-factor authentication, encrypting sensitive data in transit, strengthening API security, and improving monitoring capabilities to detect suspicious activities.

## Findings 
The assessment identified several security risks that could impact the confidentiality, integrity, and availability of the online banking platform. Weak authentication mechanisms increased the risk of unauthorized access, while exposed APIs and insecure communication channels could potentially be exploited by attackers.

The exercise also demonstrated that applying structured threat modelling frameworks enables security teams to identify vulnerabilities early in the software development lifecycle, reducing the likelihood of successful attacks after deployment.

## Recommendations
Based on the assessment, the following recommendations are proposed:

* Enforce multi-factor authentication (MFA) for all customer and administrative accounts.
* Encrypt sensitive data both in transit and at rest using industry-standard encryption.
* Implement secure API authentication and authorization mechanisms.
* Perform regular threat modelling assessments whenever significant system changes occur.
* Continuously monitor authentication events and network activity for suspicious behaviour.
* Provide ongoing security awareness training to reduce the risk of phishing attacks.
* Review and update security controls regularly to address emerging threats.
  
## Lessons Learned
This threat modelling assessment demonstrated that identifying security risks during the design and development phases is more effective than addressing them after deployment. Using structured frameworks such as STRIDE, DREAD, PASTA, and MITRE ATT&CK provides a systematic approach to identifying, prioritizing, and mitigating threats.

The exercise also reinforced that threat modelling is an ongoing process rather than a one-time activity. As applications evolve and new threats emerge, organizations should continuously review their threat models to ensure that security controls remain effective and aligned with the current threat landscape.
