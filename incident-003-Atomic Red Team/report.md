## Executive Summary
Atomic Red Team is an open-source project that provides a library of focused security tests designed to emulate adversary behaviours mapped to the MITRE ATT&CK framework. Security teams can use these tests to safely simulate specific attacker techniques in a controlled environment and evaluate the effectiveness of their security controls and detection capabilities.

The project helps security professionals identify detection gaps, validate existing security controls, and improve incident response processes. By repeatedly testing how an environment responds to simulated adversary activity, organizations can identify areas for improvement before encountering similar techniques during a real-world attack.

## Objective

The objective of this investigation is to demonstrate how Atomic Red Team can be used to safely emulate adversary techniques mapped to the MITRE ATT&CK framework. The exercise aims to validate the effectiveness of security controls, identify detection gaps, and evaluate the organization’s ability to detect, investigate, and respond to simulated malicious activity.

The investigation also demonstrates how threat emulation can be used as part of a continuous security testing process, allowing security teams to move from emulating adversary behaviour to developing and validating effective detection capabilities.

## Scenario

A financial services company recently deployed a new Endpoint Detection and Response (EDR) solution and several SIEM detection rules designed to identify credential theft activities. Before undergoing a security audit, the security team wants to validate whether its security controls can effectively detect and respond to simulated adversary behaviour.

Instead of waiting for a real attack or conducting a full-scale red team engagement, the team uses Atomic Red Team to safely emulate adversary behaviour associated with the MITRE ATT&CK technique Credential Dumping (T1003).

The security analyst executes an Atomic Red Team test designed to emulate credential dumping activity in a controlled and repeatable environment. During the exercise, the SOC team monitors the environment to determine whether:

* The EDR solution detects the simulated credential dumping activity.
* Relevant Windows Event Logs are generated.
* SIEM detection rules trigger alerts as expected.
* Incident response procedures are initiated correctly.
* Analysts can accurately investigate and classify the activity.

The results of the exercise will help the organization identify potential detection gaps, validate its existing security controls, and improve its ability to detect and respond to credential-related attacks.

## Tools Used

* Atomic Red Team – Used to safely and repeatedly emulate adversary behaviour in a controlled environment for the purpose of validating security controls and detection capabilities.
* MITRE ATT&CK Framework – Used to map the simulated adversary behaviour to relevant tactics and techniques, specifically Credential Dumping (T1003).
* Windows Event Logs – Used to review system and security events generated during the Atomic Red Team test and identify evidence of suspicious activity.
* Endpoint Detection and Response (EDR) – Used to monitor endpoint activity and determine whether the simulated credential dumping behaviour was detected and alerted on.
* Security Information and Event Management (SIEM) – Used to collect and analyze security logs from the environment, search for relevant activity, and determine whether detection rules generated alerts during the emulation exercise.

## MITRE ATT&CK Mapping

The Atomic Red Team exercise was mapped to the MITRE ATT&CK framework to identify the adversary behaviour being simulated and provide a structured method for evaluating the organization’s detection capabilities.

The primary technique used in this scenario was:

* T1003 – OS Credential Dumping: Represents techniques used by adversaries to obtain credentials from an operating system.

The technique was selected because credential theft can provide attackers with access to legitimate accounts and potentially allow further compromise of an organization’s environment.

MITRE ATT&CK was used to provide context for the simulated behaviour and help the SOC team determine whether the security controls were capable of detecting activity associated with the technique.

## Investigation / Analysis

The investigation began by selecting a relevant adversary technique from the MITRE ATT&CK framework and identifying an appropriate Atomic Red Team test to safely emulate the behaviour in a controlled environment.

The Atomic Red Team test was executed to simulate credential dumping activity associated with T1003. During the exercise, the SOC team monitored the endpoint and surrounding security infrastructure for evidence of the simulated activity.

Windows Event Logs were reviewed to identify system and security events generated during the test. The EDR platform was also monitored to determine whether suspicious endpoint activity was detected and whether an alert was generated.

The relevant logs were then reviewed within the SIEM to determine whether the activity was successfully collected, correlated, and detected by existing detection rules. The SOC analyst would compare the observed activity against the expected behaviour associated with the MITRE ATT&CK technique to determine whether the alert was correctly classified.

The final stage of the analysis involved assessing the organization’s response to the simulated activity. This included determining whether an alert was generated, whether analysts could investigate the activity, and whether the appropriate incident response procedures were followed.

## Findings

The Atomic Red Team exercise demonstrated how controlled adversary emulation can be used to validate an organization’s security controls and detection capabilities.

The exercise provided an opportunity to determine whether endpoint activity associated with credential dumping could be observed through Windows Event Logs, detected by the EDR solution, and identified by SIEM detection rules.

The assessment also demonstrated that successful threat emulation requires visibility across multiple security layers. A detection gap at any stage, such as missing endpoint telemetry, inadequate log collection, or ineffective SIEM detection rules, could reduce the SOC team’s ability to identify malicious activity.

Overall, the exercise provided a controlled method for identifying potential weaknesses in the organization’s detection and response capabilities before similar activity occurs during a real attack.

## Recommendations

Based on the findings of the exercise, the following recommendations are proposed:

* Regularly perform Atomic Red Team tests to validate security controls against relevant MITRE ATT&CK techniques.
* Ensure that important Windows security logs and endpoint telemetry are properly collected and available to the SIEM.
* Review and improve SIEM detection rules based on the results of threat emulation exercises.
* Ensure that EDR solutions are configured to detect suspicious credential access and credential dumping behaviour.
* Map detection rules to relevant MITRE ATT&CK techniques to identify areas where detection coverage is limited.
* Document the results of each emulation exercise and track identified detection gaps until they are resolved.
* Conduct periodic validation exercises to ensure that previously implemented detections continue to function as expected.
* Use the results of threat emulation exercises to improve SOC analyst investigation and incident response procedures.

## Lessons Learned

The Atomic Red Team exercise demonstrated that security controls should not simply be deployed and assumed to be effective. They should be continuously tested and validated against realistic adversary behaviour.

The exercise also reinforced the relationship between threat emulation and detection. Atomic Red Team can be used to safely generate adversary-like activity, while Windows Event Logs, EDR, and SIEM platforms provide the visibility required for security teams to identify and investigate that activity.

MITRE ATT&CK provides a structured framework for understanding the behaviour being emulated and allows organizations to measure and improve their detection coverage against known adversary techniques.

Most importantly, the exercise demonstrated that discovering a detection gap during a controlled security test is valuable because it gives the organization an opportunity to improve its defenses before a real attacker exploits the same weakness.
