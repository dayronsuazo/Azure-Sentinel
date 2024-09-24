# Azure Sentinel
Setting up Microsoft Sentinel for SOC Analyst experience

## Objective
In this lab, I will firstly sign up for an **Azure subscription**. I will then create a **Virtual Machine (honeypot)** in the Azure environment and turn off all external and Windows firewalls so it is exposed to the Internet making it very discoverable (enticing to attackers).
My next step will be to set up a **log repository (Log Analytics Workspace)** which will be used to ingest the logs from the VM and finally set up **Azure Sentinel** to create a map, that maps all different attacking data.
I will also be using PowerShell to extract the IP Address from the Windows logs and send  it to a third party API which will then send it back to our VM, to create a custom log with data.

### Skills Learned
**Log Analysis**
By creating the VM, I was able to see what a failed log on attempt looks like by checking Windows Event Viewer>Audit Failure>Event ID 4625.
This Event ID also provides network information such as:
Workstation Name and source IP Address

**Scripting**
Used Powershell ISE to look through event logs, grab all events of people who failed to log in, grab their IP Address, get their geo data and create a new log file.

I will be using "ipgeolocation.io IP lookup database" to identify where users are attempting to log in from.

### Tools Used
[Bullet Points - Remove this afterwards]

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps
drag & drop screenshots here or use imgur and reference them using imgsrc

Every screenshot should have some text explaining what the screenshot is about.

Example below.

*Ref 1: Network Diagram*
