# <B> Security Operations Center Homelab</B>
![labhome](https://github.com/user-attachments/assets/6ca1d2a8-c33e-4ef5-83ec-0e3f1aae4362)


## <B>Overview</B>

 This project is my deep dive into hands-on security operations. In this **Security Operations Center (SOC) lab**, I have set up a **honeypot**—a virtual machine exposed to the internet—to attract attackers and analyze intrusion attempts. This lab is an opportunity to strengthen my cybersecurity expertise, experiment with security tools, and better understand real-world threats.

## <B>What I Built</B>

- 🌐 <B>Honeypot Deployment</B>: A virtual machine designed to attract and monitor cyber attacks.
- 🔍 <B>Log Management</B>: Collecting and analyzing security logs using Azure Monitor.
- 📊 <B>SIEM Integration</B>: Connecting logs to <B>Microsoft Sentinel</B> for in-depth security analysis.
- 🗺️ <B>Geographic Visualization</B>: Tracking attacker locations with Azure Workbooks.

---

## <B>Getting Started</B>

### <B>Prerequisites</B>

Before diving into the lab, I made sure I had:

- An <B>Azure account</B> ([Sign up here](https://portal.azure.com/)).
- <B>Azure CLI</B> installed ([Installation Guide](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)).
- <B>Contributor or Owner</B> role in my Azure subscription.

---

## <B>Step-by-Step Guide</B>

### <B>1. Creating a Free Azure Subscription</B>
- Signed up at [Azure Portal](https://portal.azure.com/).
- Verified my identity and set up billing (Azure provides free credits for new users).

### <B>2. Setting Up the Virtual Machine (VM)</B>
- Navigated to <B>Azure Virtual Machines</B>.
- Clicked <B>Create</B> > <B>Virtual Machine</B>.
- Chose an appropriate image (e.g., Ubuntu, Windows Server) and VM size.
- Configured networking for public internet access.
- Set up administrator credentials and deployed the VM.

### <B>3. Viewing Raw Logs on the Virtual Machine</B>
- Connected to the VM using SSH or RDP.
- Inspected system logs (`/var/log/auth.log` for Linux, Event Viewer for Windows).
- Identified failed login attempts and suspicious activity.

### <B>4. Creating a Log Repository - Log Analytics Workspace</B>
- Created a new <B>Log Analytics Workspace</B> in <B>Azure Monitor</B>.
- Configured data retention and storage settings.
- Ensured logs were being collected from the VM.

### <B>5. Connecting the VM to Log Analytics Workspace</B>
- Installed the <B>Azure Monitoring Agent</B> on the VM.
- Linked the VM to the <B>Log Analytics Workspace</B>.
- Verified log collection by querying logs in <B>Log Analytics</B>.

### <B>6. Configuring the Azure Monitor Agent - Security Event Connector</B>
- Set up the **Azure Monitor Agent** in **Microsoft Sentinel**.
- Configured the **Security Events Connector** to establish a connection between my VM and Log Analytics Workspace.
- Ensured logs were being forwarded to **Microsoft Sentinel** for analysis.

### <B>7. Querying Logs with KQL</B>
- Used <B>Kusto Query Language (KQL)</B> to analyze logs.
- Queried failed login attempts and identified attacker patterns.
- Saved useful queries for continuous monitoring.

### <B>8. Uploading Geolocation Data to SIEM</B>
- Collected attacker IP addresses from logs.
- Used third-party IP geolocation services (e.g., MaxMind, ipinfo.io) to map locations.
- Stored enriched logs in <B>Microsoft Sentinel</B>.

### <B>9. Inspecting Enriched Logs - Tracking Attackers</B>
- Viewed enriched log data in <B>Microsoft Sentinel</B>.
- Identified trends in attacker locations and behavior.
- Adjusted security policies based on insights.

### <B>10. Creating a Live Attack Map</B>
- Used <B>Azure Workbooks</B> to create a real-time attack visualization.
- Mapped attack sources on a <B>geographic dashboard</B>.
- Customized data views for deeper insights.

### <B>11. Beyond the Lab - Creating Security Incidents</B>
- Set up <B>Microsoft Sentinel Incidents</B> to detect threats.
- Automated alerts for suspicious activity.
- Explored next steps for expanding my SOC lab.

---

## <B>What’s Next?</B>

- Verifying deployment in the <B>Azure Portal</B>.
- Accessing the virtual machine via SSH: `ssh adminuser@<public-ip>`.
- Exploring log data in <B>Microsoft Sentinel</B>.
- Experimenting with automation and detection rules to strengthen security defenses.

## <B>Why This Matters to Me</B>

Cybersecurity is constantly evolving, and I love staying ahead of the curve. This lab isn't just a technical exercise, it's an opportunity to apply real-world security concepts, think like an attacker, and defend like a SOC analyst. I’m always looking to improve my skills, explore new security tools, and dive deeper into cyber threat detection.

## <B>Contributions</B>

I’d love to connect with fellow cybersecurity enthusiasts! Feel free to fork this repository, contribute, or reach out with any insights or feedback!

