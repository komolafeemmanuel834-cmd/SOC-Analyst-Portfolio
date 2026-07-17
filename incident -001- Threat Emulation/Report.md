# Incident 001 - Threat Emulation

## Objective
The objective of this investigation is to analyze an emulated cyber attack, understand the tactics and techniques used by the threat actor, identify indicators of compromise (IOCs), and document the findings to improve future detection and response capabilities.

## Scenario
A retail organization engaged the Security Operations Center (SOC) team to conduct a threat emulation exercise to evaluate its detection and response capabilities against realistic cyber threats. Rather than waiting for a real attack, the organization proactively simulated adversary behavior based on known threat intelligence and the MITRE ATT&CK framework. During the engagement, adversary tactics, techniques, and procedures (TTPs) were selected to mirror the activities of real-world threat actors. The exercise aimed to assess the effectiveness of existing security controls, identify gaps in detection and monitoring, and measure the SOC team’s ability to detect, investigate, and respond to simulated malicious activity. The results of this engagement would be used to improve detection rules, strengthen defensive capabilities, and enhance the organization’s overall security posture.

## Tools Used
- MITRE ATT&CK Framework – Used to map adversary tactics, techniques, and procedures (TTPs).
- Atomic Red Team – Used to safely emulate individual attacker techniques.
- MITRE CALDERA – Used to automate adversary emulation based on predefined threat profiles.
- Threat Intelligence – Used to understand real-world adversary behavior and select relevant TTPs.
- TryHackMe Lab Environment – Used to complete the practical exercises and reinforce threat emulation concepts.
  
## MITRE ATT&CK Techniques
The threat emulation exercise was planned using the MITRE ATT&CK framework to replicate realistic adversary behavior. Rather than focusing on a single attack, the exercise demonstrated how threat actors progress through different stages of the attack lifecycle using known tactics and techniques.

Relevant Tactics

* Initial Access (TA0001)
* Execution (TA0002)
* Persistence (TA0003)
* Privilege Escalation (TA0004)
* Defense Evasion (TA0005)
* Credential Access (TA0006)
* Discovery (TA0007)
* Lateral Movement (TA0008)
* Collection (TA0009)
* Exfiltration (TA0010)
* Command and Control (TA0011)

These tactics were used as a reference when planning the emulation exercise to ensure realistic adversary behavior could be simulated and evaluated against the organization’s security controls.

## Investigation Steps
The threat emulation engagement began by identifying the organization’s objective of assessing its ability to detect and respond to realistic cyber threats. Relevant threat intelligence was reviewed to understand the tactics, techniques, and procedures (TTPs) commonly used by adversaries targeting organizations within the retail sector.

Using the MITRE ATT&CK framework, adversary behaviors were mapped to the different stages of the attack lifecycle. This provided a structured approach for selecting techniques that could be safely emulated during the exercise.

Threat emulation tools, including Atomic Red Team and MITRE CALDERA, were identified as suitable platforms for simulating adversary activity in a controlled environment. These tools enable security teams to replicate real-world attack techniques without causing harm to production systems.

Throughout the exercise, the planned adversary behaviors were compared against the organization’s existing security controls to determine whether malicious activity could be detected and investigated effectively. The engagement focused on identifying detection gaps, validating current monitoring capabilities, and providing recommendations to strengthen the organization’s defensive posture.

## Findings
The threat emulation exercise demonstrated the value of proactively assessing an organization’s security posture by simulating realistic adversary behavior. Mapping attack techniques to the MITRE ATT&CK framework provided a structured approach for understanding how threat actors operate and identifying potential detection gaps.

The engagement highlighted the importance of using threat intelligence to design realistic attack scenarios and validated that tools such as Atomic Red Team and MITRE CALDERA can be used to safely emulate attacker techniques. Overall, the exercise emphasized that regular threat emulation enables organizations to evaluate their monitoring capabilities and improve their readiness against real-world cyber threats.

## Recommendations
Based on the findings of this engagement, the following recommendations are proposed:

* Conduct regular threat emulation exercises to continuously evaluate the effectiveness of security controls.
* Use the MITRE ATT&CK framework to map detection rules and improve visibility across the attack lifecycle.
* Integrate threat intelligence into security operations to ensure emulated scenarios reflect current adversary techniques.
* Develop and maintain detection rules for commonly observed attacker behaviors identified during threat emulation.
* Periodically review and update incident response procedures based on lessons learned from each exercise.
* Provide continuous training for SOC analysts to strengthen detection, investigation, and response capabilities.

## Lessons Learned
This threat emulation exercise reinforced the importance of proactive security testing as part of an organization’s cyber defense strategy. Understanding adversary tactics, techniques, and procedures (TTPs) enables security teams to build more effective detection strategies and validate existing security controls before they are tested by real attackers.

The engagement also demonstrated that threat emulation is not intended to replace penetration testing or incident response, but rather to complement them by measuring an organization’s ability to detect and respond to realistic attack scenarios. Applying frameworks such as MITRE ATT&CK, together with threat intelligence and controlled emulation tools, provides a repeatable and structured approach to improving an organization’s overall security posture.

## References

- TryHackMe – Threat Emulation Module
- MITRE ATT&CK Framework (https://attack.mitre.org/)
- Atomic Red Team
- MITRE CALDERA
