The Cortex Xpanse pack for Cortex XSOAR provides full coverage of the Expanse Expander and Behavior product capabilities to allow SOCs to automate the defense of their company's attack surface. The integrations included in the pack enable fetching and mirroring of Expanse Issues into Cortex XSOAR incidents, and ingestion of indicators (IPs, domains, and certificates) referring to the corporate network perimeter as discovered by Expanse, a Palo Alto Networks company.

Through a powerful set of playbooks, analysts can correlate the discovered information with data provided from internal security systems (Palo Alto Networks Cortex Data Lake, Prisma Cloud, and Panorama, Active Directory, Splunk SIEM, etc.) to help pinpoint the right owners of assets and automate remediation.

> **Note**: This Pack, as well as its previously named **Expanse v2** Integration, were renamed to **Cortex Xpanse**. All other content items are still named the same.

##### What does this pack do?
- Provides the **Cortex Xpanse** integration (for Expanse Expander and Behavior), which allows XSOAR to collect Expanse Issues and bi-directionally mirror them. Several commands are available to search, tag, and update issues and assets in Expanse. The integration also supports the services API.
- Provides a feed integration named **Expanse Expander Feed**, which is compatible with the Cortex XSOAR Threat Intel Management capabilities to retrieve and store discovered assets (IPs, IP ranges, domains, certificates) in Cortex XSOAR for analysis and correlation.
- Provides an **Expanse Issue** incident type with dedicated fields and layouts.
- Provides a rich set of playbooks and sub-playbooks that handle the investigation and remediation of Expanse Issues.
- Provides dashboards that display the network perimeter as discovered by Expanse and the status of Expanse Issues.

##### How to use this pack?
- After the Expanse API key is added in the **Expanse v2** integration and the parameters are set, the Expanse issues will start getting mapped to the Expanse incident type and the **Handle Expanse Incident** playbook will automatically be launched.
- If you are only interested in enrichment and attribution, you can use the **Handle Expanse Incident - Attribution Only** playbook instead, by assigning it to the **Expanse Issue** incident type.
- This pack also includes a generic playbook called **Xpanse Incident Handling - Generic**. In order to use it, configure the instance without any classifier and choose **Xpanse Issue - Generic** as the incident type.

##### Screenshots

- **Expanse Incidents Dashboard**: The main dashboard for all the Expanse incidents.

    ![Expanse Incidents Dashboard](https://raw.githubusercontent.com/demisto/content/b8efd3c2e9409b02b9c4b1873ff3e783524c5104/Packs/ExpanseV2/doc_files/Expanse_Incidents_Dashboard.png)

- **Expanse Incident Layout**: The included default layout for Expanse incidents.

    ![Expanse Incident Layout](https://raw.githubusercontent.com/demisto/content/b8efd3c2e9409b02b9c4b1873ff3e783524c5104/Packs/ExpanseV2/doc_files/Expanse_Incident_Layout.png)

- **Expanse Attribution Report**: The report generated by the main playbook attribution stage after checking multiple log sources and Prisma Cloud environments.

    ![Expanse Attribution Report](https://raw.githubusercontent.com/demisto/content/b8efd3c2e9409b02b9c4b1873ff3e783524c5104/Packs/ExpanseV2/doc_files/Expanse_Attribution_Report.png)

- **Handle Expanse Incident - Remediation**: An excerpt of the remediation stage of the main playbook. Note the different branches handling notifications, automatic network remediation, and follow up Shadow IT investigation if the asset is marked as Shadow IT by the incident assignee.

    ![Handle Expanse Incident Remediation](https://raw.githubusercontent.com/demisto/content/b8efd3c2e9409b02b9c4b1873ff3e783524c5104/Packs/ExpanseV2/doc_files/Handle_Expanse_Incident_Remediation.png)

##### Video

[![Expanse and Cortex XSOAR](https://img.youtube.com/vi/I3Vj-f5VGMk/0.jpg)](https://www.youtube.com/watch?v=I3Vj-f5VGMk "Expanse and Cortex XSOAR")
