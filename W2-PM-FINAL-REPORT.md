# PENETRATION TESTING REPORT

## FOOTPRINTING & NETWORK SCANNING PHASES

### W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS

| Report Information | Details |
|---|---|
| Pentester Name | Emmanuel Jeremiah G. |
| Program/Batch | B083-Networkwalks |
| Week | Week 2 |
| Modules Completed | W2-PM2 — GHDB-Based Footprinting; W2-PM5 — Zenmap-Based Network Scanning |
| Environment | Publicly indexed web information and authorized local network |
| Phases Covered | Reconnaissance & Footprinting; Scanning & Network Discovery |

---

## 1. Liability Disclaimer

The activities documented in this report were performed for educational and cybersecurity research purposes as part of the NetworkWalks internship program.

Network scanning activities were performed within an authorized local network environment. The footprinting exercise was limited to publicly indexed information discovered through Google Search and the Google Hacking Database (GHDB). No authentication bypass, exploitation, password guessing, or unauthorized modification of systems was performed.

The techniques and information documented in this report should only be used on systems, networks, and resources for which appropriate authorization has been obtained. Unauthorized access to computer systems or networks may violate applicable laws and regulations.

---

## 2. Introduction

This report documents the Week 2 practical activities completed as part of the NetworkWalks Cybersecurity Internship. The activities covered two important stages of cybersecurity assessment: reconnaissance and footprinting, followed by network scanning and host discovery.

The first module, W2-PM2, focused on GHDB-based footprinting. The Google Hacking Database and advanced Google search operators were used to identify publicly indexed information relevant to the assigned tasks. The practical demonstrated how carefully constructed search queries can assist information gathering without directly interacting with or exploiting a target system.

The second module, W2-PM5, focused on network scanning using Zenmap, the graphical user interface for Nmap. The practical involved identifying the local IPv4 configuration and subnet, discovering live hosts, identifying IP and MAC addresses, viewing the network topology, and preserving the topology as a PDF.

Together, the two modules demonstrated how publicly available information and network discovery techniques can contribute to the reconnaissance and scanning phases of a security assessment.

---

## 3. Tools Used

| Tool / Component | Purpose |
|---|---|
| Google Search | Executing advanced search queries and reviewing publicly indexed information |
| Google Hacking Database (GHDB) | Identifying Google dorks relevant to footprinting tasks |
| Web Browser | Accessing GHDB, performing searches, and reviewing indexed results |
| Zenmap / Nmap | Network discovery and scanning |
| Npcap | Providing packet capture and network access support required by Nmap on Windows |
| Windows Command Prompt | Examining the Windows network configuration |
| ipconfig /all | Identifying IPv4 address, subnet mask, gateway, and physical address |
| Mobile Hotspot / Local Network | Providing the controlled network environment used for the final network scan |
| Microsoft Print to PDF | Saving the network topology as a PDF |
| GitHub | Documenting the practical activities and preserving project evidence |

---

## 4. Activities Performed

### 4.1 W2-PM2 — GHDB-Based Footprinting

The first practical activity involved using the Google Hacking Database and Google Search for passive footprinting.

GHDB contains advanced Google search queries, commonly referred to as Google dorks, which use search operators such as intitle, inurl, and filetype to locate specific types of information already indexed by search engines.

The activity was performed as passive information gathering. Search results were reviewed without attempting to bypass authentication, exploit discovered systems, guess credentials, or modify any resource.

### Task 1 — Security Camera Search

The first task required the identification of publicly indexed results associated with security-camera web interfaces.

The Google Hacking Database was reviewed to identify relevant search queries. One of the queries examined was:

intitle:"webcamXP" inurl:8080

The query returned multiple indexed results associated with webcamXP interfaces. Additional camera-related dorks were also tested during the practical.

Some indexed results opened successfully and displayed web interfaces, while others were unavailable, refused connections, redirected to search pages, or did not contain information relevant to the task.

This demonstrated an important limitation of search-engine footprinting: the presence of a URL in a search index does not guarantee that the resource remains available, relevant, vulnerable, or authorized for further security testing.

### Task 2 — Mathematics PDF Search

The second GHDB task involved identifying listings containing downloadable mathematics material in PDF format.

Directory-index and file-type search queries were used and refined for different mathematical subjects. Examples of the search patterns included:

intitle:index of "parent directory" mathematics pdf

intitle:"Index of" calculus filetype:pdf

intitle:"Index of" "Linear Algebra" filetype:pdf

intitle:"Index of" algebra filetype:pdf

intitle:"Index of" "Abstract Algebra" filetype:pdf

intitle:"Index of" geometry filetype:pdf

The search process identified multiple publicly indexed directories containing mathematics-related PDF material. Search results were manually reviewed because some results contained examination papers, lecture materials, research papers, individual chapters, or unrelated documents rather than the type of resource required by the task.

The exercise demonstrated that Google dorking requires more than executing a search query. Search results must be reviewed and validated for relevance because search-engine indexing does not guarantee that every returned result satisfies the intended search objective.

### W2-PM2 Observation

The GHDB practical demonstrated how search operators can improve the precision of passive information gathering. It also showed the importance of distinguishing between discovering publicly indexed information and having authorization to perform additional security testing against the discovered resource.

No exploitation or authentication bypass was performed during this module.

---

### 4.2 W2-PM5 — Network Scanning with Zenmap

The second practical activity involved using Zenmap to perform network discovery within a local network environment.

The assigned tasks required the installation of Zenmap, identification of the local IP address and subnet, discovery of live hosts, identification of their IP and MAC addresses, and creation of a network topology.

### Zenmap Installation

Nmap and Zenmap were obtained from the official Nmap source for installation on the Windows PC. Npcap was also installed as the packet capture and network access component required by Nmap on Windows.

The installation initially presented a challenge. Installer files downloaded on another device and transferred to the Windows PC produced NSIS integrity errors when executed. Different transferred copies were tested, but the error persisted.

Instead of bypassing the integrity verification, a fresh copy of the installer was downloaded directly from the official source using the same Windows PC on which Zenmap was to be installed. The directly downloaded installer executed successfully.

During Npcap installation, WinPcap API-compatible mode was enabled, while the options to restrict Npcap driver access to administrators and support raw 802.11 traffic were left unchecked.

Zenmap and Npcap were subsequently installed successfully.

### Initial Network Identification

The Windows Command Prompt and the ipconfig /all command were used to examine the active Wi-Fi adapter.

The initial school Wi-Fi network used the subnet mask:

255.255.0.0

This corresponds to a /16 network. The network was identified as:

172.18.0.0/16

A /16 IPv4 subnet contains 65,536 total addresses, which is substantially larger than a /24 subnet containing 256 total addresses.

A Zenmap Quick Scan was initially attempted on the school Wi-Fi network. Because of the large /16 address space, the scanning process took significantly longer than expected.

During the scan, multiple IP addresses also appeared with the same RouterBOARD MAC address. Consequently, those results could not simply be interpreted as separate physical hosts.

Rather than relying on ambiguous results from the larger institutional network, the scanning exercise was moved to a smaller and more controlled mobile-hotspot environment.

### Controlled Mobile-Hotspot Network

After connecting the Windows PC to the mobile hotspot, ipconfig /all was used again to verify the network configuration.

The Windows PC received the following configuration:

| Parameter | Value |
|---|---|
| IPv4 Address | 10.206.203.243 |
| Subnet Mask | 255.255.255.0 |
| CIDR Prefix | /24 |
| Default Gateway | 10.206.203.175 |
| PC Physical Address | EC-5C-68-7F-EB-D9 |

The /24 network provided a smaller and more manageable address space for the practical.

### Live Host Discovery

Zenmap was configured with the target:

10.206.203.243/24

The Quick Scan profile generated the following Nmap command:

nmap -T4 -F 10.206.203.243/24

The scan completed successfully and reported:

256 IP addresses (2 hosts up) scanned in 23.78 seconds

The following live hosts were identified:

| Host | IP Address | Status |
|---|---|---|
| Host 1 | 10.206.203.175 | Up |
| Host 2 | 10.206.203.243 | Up |

The /24 scan completed significantly faster and produced results that were easier to interpret than the earlier /16 scan.

### MAC Address Identification

The MAC addresses associated with the discovered hosts were identified using Zenmap scan information and the Windows network configuration.

| IP Address | MAC Address | Evidence Source |
|---|---|---|
| 10.206.203.175 | 22:E8:17:DC:40:66 | Zenmap / Nmap scan result |
| 10.206.203.243 | EC-5C-68-7F-EB-D9 | Windows ipconfig /all |

The MAC address for 10.206.203.175 was obtained from the Zenmap host information, while the physical address of the Windows PC at 10.206.203.243 was confirmed through ipconfig /all.

### Network Topology

After the scan was completed, the Topology tab in Zenmap was used to display the discovered network visually.

The topology showed the two discovered hosts:

10.206.203.175

10.206.203.243

The displayed topology was captured and preserved as a PDF using Microsoft Print to PDF, completing the final requirement of the Zenmap practical.

---

## 5. Risk Analysis / Impact

The observations below are based on the footprinting and network-scanning exercises.

| No. | Finding / Observation | Evidence | Potential Impact | Risk Level |
|---|---|---|---|---|
| 1 | Publicly indexed web interfaces and resources can be discovered through targeted search queries | GHDB and Google Search returned indexed resources matching specific search operators | Publicly exposed information may assist reconnaissance by revealing resources that an organization did not intend to make easily discoverable | Low |
| 2 | Search engines may retain references to resources that are no longer available or relevant | Some indexed results redirected, refused connections, or no longer provided the expected content | Stale indexing can create misleading reconnaissance information and demonstrates the need to validate findings before drawing conclusions | Informational |
| 3 | Active hosts were discoverable within the controlled local network | Zenmap identified 2 live hosts within the /24 network | Host discovery provides information about devices participating in a network and may assist further authorized network assessment | Low |
| 4 | IP and MAC address information was observable during local network discovery | Zenmap and ipconfig /all provided IP and MAC information | Network addressing information can assist asset identification and network mapping during an authorized assessment | Low |
| 5 | Network topology could be derived from scan results | Zenmap topology displayed the discovered hosts | Network topology information can improve understanding of the structure of a network and therefore should be handled appropriately | Low |

### Risk Interpretation

The findings above are observations from reconnaissance and network-discovery activities and should not be interpreted as confirmed vulnerabilities.

The practical primarily involved passive information gathering, network configuration identification, and host discovery. No exploitation or vulnerability validation was performed as part of W2-PM2 or W2-PM5.

The discovery of an indexed URL, IP address, MAC address, open service, or other technical information does not by itself demonstrate that a system is vulnerable. Further testing within an explicitly authorized scope would be required before a vulnerability could be confirmed.

---

## 6. Recommendations

Based on the observations made during the Week 2 activities, the following security practices are recommended:

### 1. Review Publicly Indexed Information

Organizations should periodically review what information about their systems and resources can be discovered through public search engines.

### 2. Remove Unnecessary Public Exposure

Web interfaces, directories, files, and services that are not intended for public access should be appropriately restricted and removed from unnecessary exposure.

### 3. Apply Appropriate Authentication and Access Controls

Administrative interfaces and sensitive resources should be protected using appropriate authentication and access-control mechanisms rather than relying on obscurity or lack of search-engine visibility.

### 4. Maintain an Accurate Asset Inventory

Organizations should maintain an up-to-date inventory of authorized systems and network devices so that unexpected devices can be identified more easily.

### 5. Perform Authorized Internal Network Discovery

Periodic network discovery can help administrators identify active hosts and compare discovered devices against the organization's approved asset inventory.

### 6. Investigate Unexpected Network Devices

Any device that appears unexpectedly during an authorized network scan should be investigated and verified before being considered trusted.

### 7. Maintain Network Documentation

IP addressing, device information, network topology, and other relevant infrastructure documentation should be maintained and updated when changes occur.

### 8. Validate Reconnaissance Findings

Search-engine and scanning results should be reviewed carefully before conclusions are made. An indexed result or detected network response should be treated as an observation until it has been appropriately validated.

### 9. Maintain Authorization and Scope

Reconnaissance, network scanning, vulnerability assessment, and other security-testing activities should only be performed against systems and networks where appropriate authorization and scope have been established.

---

## 7. Conclusion

During Week 2 of the NetworkWalks Cybersecurity Internship, I completed practical activities covering reconnaissance, footprinting, and network scanning.

In W2-PM2, I used the Google Hacking Database and advanced Google search operators to identify publicly indexed information. The exercise improved my understanding of operators such as intitle, inurl, and filetype and demonstrated how targeted search queries can support passive reconnaissance.

The exercise also demonstrated that a search result must be evaluated carefully. Some indexed resources were unavailable, irrelevant, or no longer provided the expected content. I therefore learned that the discovery of information through a search engine does not automatically establish that the information is currently valid, that a system is vulnerable, or that further interaction with the system is authorized.

In W2-PM5, I used Zenmap and Nmap to examine a local network environment. I identified the local IPv4 configuration and subnet, performed host discovery, identified two active hosts, determined their IP and MAC addresses, and generated a network topology.

The initial school Wi-Fi /16 network also provided an important practical lesson. Its significantly larger address space increased the scanning workload, and the appearance of the same RouterBOARD MAC address across multiple IP addresses made the results difficult to interpret. Moving the practical to a controlled /24 mobile-hotspot network produced a smaller and clearer environment for completing the assigned discovery tasks.

The Week 2 exercises strengthened my understanding of the relationship between reconnaissance and network scanning. Reconnaissance can reveal useful publicly available information before direct interaction with a target, while network scanning can provide information about active hosts and network structure within an authorized environment.

The practical also reinforced the importance of troubleshooting and evidence-based analysis. Rather than bypassing installer integrity errors or automatically accepting unusual scan results, I investigated the problems, changed the environment where appropriate, and verified findings using available evidence.

Finally, the exercises reinforced the importance of authorization and scope in cybersecurity. Information gathering and network scanning are useful security-assessment techniques, but they must be conducted responsibly and within authorized boundaries.

---

## 8. Evidence Collected

Detailed screenshots and supporting evidence for the Week 2 practical activities are available in the main project documentation within this repository.

The evidence includes:

- GHDB entries and Google dork search results used during W2-PM2.
- Examples of reviewed publicly indexed resources.
- Unsuccessful or irrelevant search results encountered during footprinting.
- Windows network configuration showing the initial school Wi-Fi /16 subnet.
- Zenmap evidence from the initial /16 scanning attempt.
- Network configuration from the controlled mobile-hotspot /24 network.
- Zenmap Quick Scan configuration and completed scan output.
- Evidence showing the 2 discovered live hosts.
- Zenmap host information showing the MAC address associated with 10.206.203.175.
- Windows ipconfig /all evidence showing the physical address associated with 10.206.203.243.
- Zenmap network topology showing the discovered hosts.
- The generated network-topology PDF.

### Network Topology PDF

[Task7-Zenmap-Network-Topology.pdf](https://github.com/user-attachments/files/32656788/Task7-Zenmap-Network-Topology.pdf)

---

## Report Summary

**Intern:** Emmanuel Jeremiah G.  
**Program/Batch:** B083-Networkwalks  
**Week:** 2  
**Completed Modules:** W2-PM2, W2-PM5 and W2-PM-FINAL  
**Areas Covered:** Reconnaissance, Footprinting, Network Discovery and Network Scanning  
**Status:** Completed
