## Executive Summary
The Elastic Stack is a search and analysis platform designed to help analysts manage data from a wide variety of sources, forming the foundation of the modern Security Information and Event Management (SIEM) solution. The Elastic Stack is a collection of technologies used to ingest, store, search, analyze, and visualize data from a wide variety of sources. It can serve as the foundation for security monitoring and SIEM capabilities.. The Elastic stack consists of the following components:
* Elasticsearch - The core search engine and data store of the Elastic Stack
* Kibana - The graphical user interface of the Elastic Stack.
* Elastic Agent – a single, lightweight agent used to collect and forward telemetry from endpoints and other sources to the Elastic Stack, centrally managed through Fleet.
* Fleet Server - the centralized management interface for Elastic Agents, accessible through Kibana.

## Objective 
The objective of this investigation is to deploy and configure a functional Elastic-based SOC monitoring environment capable of collecting, centralizing, and analyzing security and web-server telemetry. The lab aims to demonstrate the deployment of Elasticsearch, Kibana, Fleet Server, and Elastic Agent, while also validating Apache and custom log ingestion.

The investigation also aims to demonstrate how security analysts can use Kibana to explore logs, create visualizations, build dashboards, and establish a foundation for threat detection and security investigations.

## Scenario
A growing organization wanted to establish a basic Security Operations Center (SOC) capability to improve its visibility into endpoint activities and security events across its environment. However, the organization lacked a centralized platform for collecting, storing, and analyzing logs from its systems. As a result, security investigations were time-consuming, and potentially suspicious activities could go unnoticed due to the absence of centralized monitoring.

To address this challenge, a SOC lab was designed to simulate the deployment of a modern security monitoring infrastructure. The objective was to build an environment capable of ingesting endpoint telemetry, managing security agents, and providing analysts with a centralized interface for monitoring and investigation.

The proposed solution involved deploying the Elastic Stack to serve as the organization's logging and visualization platform. To enable scalable endpoint monitoring, a Fleet Server would be configured to centrally manage Elastic Agents deployed across endpoints. These agents would collect system and security telemetry and forward it to the Elastic environment for analysis.

By implementing this architecture, the organization would gain improved visibility into endpoint activity, establish a foundation for threat detection and investigation, and create a realistic SOC environment for security monitoring and incident response exercises.

## Tools Used
* Elasticsearch - Serves as the central repository for storing and indexing logs and security events.
* Kibana - Serves as the graphical user interface, thereby Providing dashboards, visualizations, and investigative capabilities for security analysts.
* Fleet Server - Centrally manages Elastic Agents and distributes monitoring policies across endpoints.
* Elastic Agents - Collects endpoint logs, metrics, and security telemetry for analysis.
* Linux Terminal - Enables installation, configuration, and administration of Elastic Stack components.
* Apache Web Server – Used as the source of web-server logs for demonstrating log collection, ingestion, and analysis within the Elastic environment.
* Web Browser - Provides access to the Kibana interface for monitoring and management activities.

## SOC Lab Architecture 
   Web Application
          │
          │ Apache Web Logs
          ▼
     Elastic Agent
          │
          ▼
      Fleet Server
          │
          ▼
     Elasticsearch
          │
          ▼
        Kibana
          │
     ┌────┴────┐
     ▼         ▼
 Dashboards  Visualisations

 ## Implementation 
 The deployment began with the installation and configuration of Elasticsearch and Kibana through the Linux terminal. Once the services were successfully configured, Kibana was accessed through a web browser using the host IP address and port 5601, providing access to the Elastic management interface.

Following the successful deployment of the Elastic Stack, a Fleet Server was configured within Kibana to facilitate centralized management of Elastic Agents. The Fleet Server was enrolled and verified to ensure proper communication with the Elastic environment. An Elastic Agent was subsequently created and deployed to the endpoint, enabling the collection of system telemetry and security-related events. Once enrolled, the agent appeared within the Fleet interface, confirming successful connectivity between the endpoint and the Elastic Stack.

To expand the lab's monitoring capabilities, Apache web server logs were integrated into the environment. This integration enabled the collection and analysis of web server activity, allowing visibility into HTTP requests, response codes, client connections, and other web-related events. The ingestion of Apache logs demonstrated how security analysts can monitor web infrastructure and identify potentially suspicious activity through centralized logging.

In addition to standard integrations, custom log ingestion was configured to allow the collection of organization-specific log sources. This process involved defining custom log paths and ensuring that the Elastic Agent could successfully collect and forward the data to Elasticsearch. The implementation of custom logs highlighted the flexibility of the Elastic Stack in supporting a wide range of data sources beyond default integrations.

After log ingestion was validated, the collected data was explored within Kibana using the Discover interface. This allowed for verification of incoming events and provided insight into the structure and content of the logs being received from both Apache and custom data sources.

To improve visibility and support security monitoring activities, multiple visualizations were created within Kibana. These visualizations transformed raw log data into meaningful graphical representations, enabling easier identification of trends, anomalies, and system activity. Metrics such as event volume, log source distribution, and web server activity could be observed more efficiently through visual analysis.

Finally, a dashboard was developed to consolidate key visualizations into a single monitoring interface. The dashboard provided a centralized view of the environment, allowing analysts to quickly assess system activity, monitor log ingestion status, and investigate events of interest. This completed the SOC lab implementation by providing both data collection and visualization capabilities required for effective security monitoring and analysis.

The successful deployment of Elasticsearch, Kibana, Fleet Server, Elastic Agent, Apache log integration, custom log ingestion, visualizations, and dashboards established a functional SOC lab capable of supporting centralized log analysis, security monitoring, and future threat detection and investigation exercises.

## Findings
* Elasticsearch and Kibana were successfully deployed and configured, providing a centralized platform for log management and analysis.
* Fleet Server and Elastic Agent enrollment enabled centralized endpoint monitoring and management.
* Apache logs and custom logs were successfully ingested into the Elastic Stack, demonstrating the platform's ability to handle multiple log sources.
* Kibana visualizations and dashboards improved visibility into collected data and simplified log analysis.
* The SOC lab provided a functional environment for security monitoring, investigation, and future threat detection exercises.
## Recommendations
* Enable additional log sources such as Sysmon, Windows Security Logs, and firewall logs to improve visibility.
* Develop detection rules and alerts for suspicious activities identified within the environment.
* Regularly review dashboards and visualizations to ensure they remain relevant to monitoring objectives.
* Conduct periodic testing of agent connectivity and log ingestion to maintain data integrity.
* Expand the lab environment to include multiple endpoints and additional security data sources.
* Implement role-based access controls (RBAC) to ensure analysts only have access to the data and administrative functions required for their responsibilities.
* Establish alerting and detection rules for suspicious web activity, authentication anomalies, unusual processes, and other relevant security events.
## Lessons Learned
* Proper configuration of Fleet Server is essential for successful agent enrollment and centralized management.
* Centralized logging significantly improves visibility and simplifies security investigations.
* Data visualization enhances an analyst's ability to identify trends and anomalies quickly.
* Integrating multiple log sources provides a more comprehensive view of system activity.
* Building a SOC lab offers practical experience with security monitoring tools and log management workflows.
* Log collection alone is not sufficient for effective security monitoring. Collecting telemetry provides visibility, but analysts must also develop detection rules, alerts, dashboards, and investigation workflows to turn raw data into actionable security intelligence.

