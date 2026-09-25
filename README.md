# 🔐 NetworkWalks Cybersecurity Internship — Week 2

## Footprinting & Network Scanning

**Program/Batch:** B083-Networkwalks  
**Intern:** Emmanuel Jeremiah G.  
**Week:** 2  
**Domain:** Cybersecurity  

---

## 📌 Project Overview

This repository documents the practical activities completed during Week 2 of the NetworkWalks Cybersecurity Internship.

The week focused on two key phases of cybersecurity assessment: **footprinting** and **network scanning**. The practical work involved using the Google Hacking Database (GHDB) and advanced Google search operators for information discovery, followed by network discovery and scanning using Zenmap.

### Project Modules

| Module | Project | Status |
|---|---|---|
| W2-PM2 | GHDB-Based Footprinting | ✅ Completed |
| W2-PM5 | Zenmap-Based Network Scanning | ✅ Completed |
| W2-PM-FINAL | Week 2 Documentation & Report | ✅ Completed |

---

## 🔎 W2-PM2 — GHDB-Based Footprinting

### Objective

The objective of this project was to perform passive footprinting using the **Google Hacking Database (GHDB)** and advanced Google search operators (Google Dorks) to identify publicly indexed information available on the Internet.

The practical exercise consisted of two tasks:

1. Identifying publicly indexed web interfaces related to security cameras using relevant Google Dorks.
2. Identifying directory listings containing downloadable mathematics eBooks in PDF format.

> **Note:** The activities in this project were limited to information publicly indexed by search engines. No authentication bypass, exploitation, credential guessing, or unauthorized modification of systems was performed.

### Tools Used

| Tool / Platform | Purpose |
|---|---|
| Google Search | Executing advanced search queries and reviewing indexed results |
| Exploit-DB GHDB | Identifying and studying Google Dorks relevant to footprinting |
| Web Browser | Reviewing publicly accessible search results |
| Microsoft Word | Recording and organizing project findings |

---

### Task 1 — Security Camera Footprinting

The first task involved using GHDB and relevant Google Dorks to identify publicly indexed web interfaces associated with network cameras and webcam services.

One of the primary search patterns used during the practical was:

`intitle:"webcamXP" inurl:8080`

Additional GHDB entries and search patterns were examined during the reconnaissance process. I reviewed the search results and documented relevant findings in the project worksheet.

#### GHDB Dork Identification
The Google Hacking Database was reviewed to identify relevant search queries for the footprinting exercise.
<img width="1920" height="1040" alt="Task1-GHDB-WebcamXP-Dork-Entry" src="https://github.com/user-attachments/assets/d75351aa-1596-4de6-834a-a09bffecf1f4" />

#### Google Dork Search
The selected dork was executed in Google Search to identify publicly indexed results associated with webcamXP.
<img width="1920" height="1040" alt="Task1-GHDB-WebcamXP-Google-Dork-Search" src="https://github.com/user-attachments/assets/72f31e67-957a-4780-8317-c5831cd9d892" />


#### Task 1 Findings
| No. | Link | Relevant Dork | Username/Password (if any) |
|---:|---|---|---|
| 1 | http://122.116.41.8:8080/ | intitle:"webcamXP" inurl:8080 | --- |
| 2 | http://109.233.191.130:80/ | intitle:"webcamXP" | --- |
| 3 | http://199.114.240.169 | intitle:"Webcam" inurl:WebCam.htm | --- |
| 4 | http://72.199.200.5:8080/ | intitle:"webcamXP" inurl:8080 | --- |
| 5 | http://139.64.168.120:8080/ | intitle:"webcamXP" inurl:8080 | --- |
| 6 | http://109.233.191.130:8080/ | intitle:"webcamXP" inurl:8080 | --- |
| 7 | http://75.149.26.30:1024/ | intitle:"webcamXP" inurl:8080 | --- |
| 8 | http://104.8.232.105:8081/ | intitle:"webcamXP" inurl:8080 | --- |
| 9 | http://85.93.53.175:8080/ | intitle:"webcamXP" inurl:8080 | --- |
| 10 | http://109.233.191.130:8080/ | intitle:"webcamXP" inurl:8080 | --- |

#### Result Review
Some of the indexed results were opened during the practical to determine whether the referenced web interface was still accessible.
<img width="1920" height="1040" alt="Task1-WebcamXP-109 233 191 130-Accessible" src="https://github.com/user-attachments/assets/16a08fa2-8e5c-4c10-b7df-1074b2c5749a" />



### Observations

The exercise demonstrated how specially crafted search queries can narrow publicly indexed information to particular technologies, page titles, URL patterns, and services.

During the practical, some search queries produced useful results while others produced irrelevant or inaccessible results. This showed that a Google Dork identifies indexed information but does not guarantee a result will remain available or accessible when reviewed.

No usernames or passwords were used during the exercise.

---

### Task 2 — Mathematics eBook PDF Footprinting

The second task involved using advanced Google search operators to identify publicly indexed directory listings containing downloadable mathematics eBooks in PDF format.

Search operators such as `intitle:` and `filetype:` were used together with mathematics-related keywords to narrow the search results. The results were reviewed to distinguish actual eBook collections from unrelated materials such as examination papers, course documents, syllabi, individual research papers, and incomplete document collections.

#### Task 2 Findings

| No. | Link | Relevant Dork | Username/Password (if any) |
|---:|---|---|---|
| 1 | https://www.skylineuniversity.ac.ae/pdf/math/ | intitle:index of "parent directory" mathematics pdf | --- |
| 2 | http://erewhon.superkuh.com/library/Math/ | intitle:index of "parent directory" mathematics pdf | --- |
| 3 | https://education.giakonda.org.uk/Maths/ | intitle:index of "parent directory" mathematics pdf | --- |
| 4 | https://ochicken.net/library/Mathematics/ | intitle:index of "parent directory" mathematics pdf | --- |
| 5 | https://download.tuxfamily.org/openmathdep/calculus/ | intitle:"Index of" calculus filetype:pdf | --- |
| 6 | https://lira.epac.to/DOCS-TECH/Math/Linear%20Algebra/ | intitle:"Index of" "Linear Algebra" filetype:pdf | --- |
| 7 | https://download.tuxfamily.org/openmathdep/algebra/ | intitle:"Index of" algebra filetype:pdf | --- |
| 8 | https://download.tuxfamily.org/openmathdep/algebra_abstract/ | intitle:"Index of" "Abstract Algebra" filetype:pdf | --- |
| 9 | https://download.tuxfamily.org/openmathdep/algebra_linear/ | intitle:"Index of" "Linear Algebra" filetype:pdf | --- |
| 10 | https://download.tuxfamily.org/openmathdep/geometry/ | intitle:"Index of" geometry filetype:pdf | --- |

### Observations

The search results required manual review because not every mathematics-related PDF result represented an eBook collection. Several results contained examination materials, lecture resources, research papers, individual chapters, or other academic documents rather than complete mathematics eBooks.
The exercise therefore involved not only constructing relevant Google Dorks but also evaluating the returned directory listings to determine whether they satisfied the project requirements.

---

### Challenges & Troubleshooting

During the GHDB footprinting exercise, several challenges were encountered while searching for and validating relevant results:

- Some indexed links redirected back to Google or search-result pages instead of opening the expected resource.
- Some results that appeared relevant in Google Search were no longer accessible when opened.
- Certain Google Dorks returned results that were technically related to the search terms but did not satisfy the specific project requirements.
- Several mathematics-related results contained examination papers, lecture materials, research papers, individual chapters, or other documents rather than complete eBook collections.
- Some camera-related dorks returned mostly GHDB entries, security-research pages, or other unrelated results instead of accessible camera interfaces.
- Search queries had to be refined and results manually reviewed before suitable findings could be documented.
- Previously indexed resources could change, become unavailable, or refuse connections during later attempts.

#### Irrelevant Search Results

Some camera-related Google Dorks returned results that did not satisfy the project requirement. For example, the Network Camera search produced mostly security-related pages and other unrelated results rather than the expected camera interfaces.
<img width="1920" height="1040" alt="Task1-Network-Camera-Dork-No-Relevant-Result" src="https://github.com/user-attachments/assets/955fc0d3-bfed-4b80-b3ad-8339d16a89e0" />


These challenges demonstrated that Google Dorking is not simply a matter of executing a search query. Search results must be reviewed and validated because search-engine indexing does not guarantee that a resource is currently available, relevant, or accessible.

### What I Learned

This practical helped me understand how GHDB and Google Dorks can be used during footprinting to find specific information that has been indexed by search engines. I also learned that getting a search result does not always mean the result will be useful or accessible. Some links did not work as expected, while others did not contain exactly what I was looking for, so I had to review the results carefully and refine my searches.

I also learned that finding information through Google does not automatically mean a system is vulnerable or that I have permission to perform further actions on it.

---


## 🌐 W2-PM5 — Zenmap-Based Network Scanning

### Objective
The objective of this project was to use Zenmap, the graphical user interface for Nmap, to perform network discovery and scanning within an authorized local network environment.
The practical involved identifying the local IP address and subnet, discovering live hosts within the subnet, identifying their IP and MAC addresses, and generating a network topology showing the discovered hosts.

### Project Tasks

| Task | Description | Status |
|---|---|---|
| Task 1 | Download and install Zenmap on a Windows PC | ✅ Completed |
| Task 2 | Find the local IP address and LAN subnet | ✅ Completed |
| Task 3 | Find the list of live hosts within the IP subnet | ✅ Completed |
| Task 4 | Determine the number of live hosts | ✅ Completed |
| Task 5 | Identify the IP addresses of the live hosts | ✅ Completed |
| Task 6 | Identify the MAC addresses of the live hosts | ✅ Completed |
| Task 7 | Display and save the network topology as a PDF | ✅ Completed |

### Tools Used

| Tool / Component | Purpose |
|---|---|
| Zenmap / Nmap | Network discovery and scanning |
| Npcap | Packet capture and network access support for Nmap on Windows |
| Windows Command Prompt | Viewing the computer's network configuration |
| ipconfig /all | Identifying the local IP address, subnet mask, gateway and physical address |
| Mobile Hotspot / Local Network | Providing the local network environment used during network discovery and scanning |
| Microsoft Print to PDF | Saving the network topology as a PDF |

---

### Task 1 — Zenmap Installation
The first task was to download and install Zenmap on the Windows PC. Nmap and Zenmap were obtained from the official Nmap website, while Npcap was installed as the packet capture and network access component required by Nmap on Windows.

#### Installation Challenge
The installation did not succeed on the first attempt. Installer files that had been downloaded on another device and transferred to the Windows PC produced NSIS integrity errors when executed. Different transferred copies were tested, but the same error occurred.

To resolve the issue, instead of transferring another copy of the installer, I downloaded a fresh copy directly from the official Nmap website using the same Windows PC on which Zenmap was to be installed. The directly downloaded installer ran successfully, allowing the installation to proceed.

#### Successful Installation
After obtaining the installer directly on the Windows PC, the Nmap and Zenmap installation proceeded successfully. Npcap was also installed as the packet capture and network access component required by Nmap on Windows.
During the Npcap installation, WinPcap API-compatible mode was enabled, while the options to restrict Npcap driver access to administrators and support raw 802.11 traffic were left unchecked.

The installation was completed successfully, and Zenmap was launched on the Windows PC.

#### Task 1 Result
Zenmap and Npcap were successfully installed and prepared for the network scanning exercise.

---

### Task 2 — Local IP Address and LAN Subnet
The next task was to identify the IPv4 address and LAN subnet of the Windows PC before beginning network discovery.

I used the Windows Command Prompt and the `ipconfig /all` command to examine the network configuration of the active Wi-Fi adapter.
<img width="979" height="512" alt="Task2-School-WiFi-Initial-IP-Configuration-16-Subnet" src="https://github.com/user-attachments/assets/a8c9adcd-e24e-4822-b8a1-4bed074df2c6" />

#### Initial Network Configuration
The active Wi-Fi adapter was assigned an IPv4 address within the 172.18.0.0/16 network. The subnet mask was 255.255.0.0, which corresponds to a /16 network.

Unlike the /24 network used in the instructor's demonstration, the /16 network provided a much larger address space. A /16 IPv4 subnet contains 65,536 total addresses, compared with 256 addresses in a /24 subnet.

Using the detected network configuration, I initially attempted a Zenmap Quick Scan on the school Wi-Fi network.

<img width="705" height="682" alt="Task2-Zenmap-School-WiFi-16-Quick-Scan" src="https://github.com/user-attachments/assets/f349c006-3be5-4941-a9bc-261a7ed74f42" />

#### Scanning Challenge
The initial Quick Scan on the school Wi-Fi network took significantly longer than expected because the /16 subnet covered a much larger address space. Zenmap was scanning 65,536 IPv4 addresses rather than the 256 addresses contained in a /24 subnet.

During the scan, multiple IP addresses also appeared as active with the same RouterBOARD MAC address. This made the results difficult to interpret as separate physical hosts and indicated that the network environment could be influencing the discovery results.

Rather than relying on these results, I decided to use a smaller and more controlled network environment for the remaining scanning tasks.
<img width="1920" height="1040" alt="Task2-Zenmap-School-WiFi-16-Quick-Scan (2)" src="https://github.com/user-attachments/assets/24f5eab5-666e-4fb5-870c-b33a668b1fc6" />

#### Scan Observation
While reviewing the scan results, multiple IP addresses appeared as active with the same RouterBOARD MAC address. Because the same MAC address was associated with several discovered IP addresses, the results could not simply be interpreted as separate physical hosts.

Combined with the large /16 address space and the long scanning time, this made the school Wi-Fi unsuitable for obtaining clear results for the remaining project tasks.

#### Switching to a Controlled Network
To obtain clearer and more manageable scan results, I switched the Windows PC from the school Wi-Fi network to my mobile phone hotspot.

After connecting to the hotspot, I used 'ipconfig /all' again to verify the new network configuration. The PC was assigned the IPv4 address 10.206.203.243 with the subnet mask 255.255.255.0, corresponding to a /24 network.
<img width="1920" height="1040" alt="Task2-Phone-Hotspot-IP-Configuration-24-Subnet" src="https://github.com/user-attachments/assets/bf868ff0-a0a3-4c41-82f7-4496409f912b" />

#### Task 2 Result
The local network configuration was successfully identified. The final network used for the scanning exercise was the mobile hotspot network, where the Windows PC had the IPv4 address 10.206.203.243 and a subnet mask of 255.255.255.0 (/24).

---

### Task 3 — Live Host Discovery
With the PC connected to the mobile hotspot, I used Zenmap to scan the /24 network and discover active hosts.

The target was set to 10.206.203.243/24 and the Quick Scan profile was selected. Zenmap generated and executed the following Nmap command:
nmap -T4 -F 10.206.203.243/24
<img width="1920" height="1040" alt="Task3-Zenmap-Phone-Hotspot-24-Quick-Scan" src="https://github.com/user-attachments/assets/5f3a69b5-aed0-441f-a2f0-35030d808398" />

#### Scan Result
The Quick Scan completed successfully on the /24 network. Zenmap scanned 256 IP addresses and discovered 2 active hosts.

The two live hosts identified were:
| Host | IP Address | Status |
|---|---|---|
| Host 1 | 10.206.203.175 | Up |
| Host 2 | 10.206.203.243 | Up |

The scan completed in approximately 23.78 seconds, which was significantly faster and easier to interpret than the earlier scan performed on the school Wi-Fi /16 network.
<img width="1920" height="1040" alt="Task3-Zenmap-Phone-Hotspot-24-Quick-Scan - Copy" src="https://github.com/user-attachments/assets/967e163c-5d22-4e82-8ce2-41960a40fbbd" />

### Task 4 — Number of Live Hosts
The completed Zenmap scan was reviewed to determine the number of active hosts within the scanned /24 network.

The Nmap output reported:
Nmap done: 256 IP addresses (2 hosts up) scanned in 23.78 seconds

#### Task 4 Result
A total of 2 live hosts were discovered on the network.

### Task 5 — IP Addresses of Live Hosts
The Zenmap scan results were reviewed to identify the IPv4 addresses associated with the two live hosts discovered on the network.

The following IP addresses were identified:
| Host | IP Address | Status |
|---|---|---|
| Host 1 | 10.206.203.175 | Up |
| Host 2 | 10.206.203.243 | Up |
<img width="1920" height="1040" alt="Task5-Zenmap-Live-Hosts-IP-Addresses" src="https://github.com/user-attachments/assets/7b8f0a04-7930-4755-9e1c-6a8e866a2408" />

#### Task 5 Result
The IP addresses of the 2 live hosts were successfully identified as 10.206.203.175 and 10.206.203.243.

### Task 6 — MAC Addresses of Live Hosts
The scan results and local network configuration were reviewed to identify the MAC addresses associated with the discovered hosts.

The MAC address of the host at 10.206.203.175 was identified from the Zenmap scan results, while the MAC address of the Windows PC at 10.206.203.243 was identified from the Physical Address displayed by ipconfig /all.

| IP Address | MAC Address | Source |
|---|---|---|
| 10.206.203.175 | 22:E8:17:DC:40:66 | Zenmap / Nmap scan result |
| 10.206.203.243 | EC-5C-68-7F-EB-D9 | Windows ipconfig /all |
<img width="1920" height="1040" alt="Task6-Zenmap-Host-MAC-Address-10 206 203 175" src="https://github.com/user-attachments/assets/7457f9fb-0c5d-4f91-a4af-109410eb274b" />
> **Note:** For reference, the Physical Address (EC-5C-68-7F-EB-D9) associated with 10.206.203.243 can be found in the `ipconfig /all` screenshot provided under Task 2.

The Physical Address shown in the Windows network configuration confirmed that 10.206.203.243 was the Windows PC, with the MAC address EC-5C-68-7F-EB-D9. This information had already been captured in the ipconfig /all evidence under Task 2.

#### Task 6 Result
The MAC addresses associated with the two discovered hosts were successfully identified as 22:E8:17:DC:40:66 for 10.206.203.175 and EC-5C-68-7F-EB-D9 for 10.206.203.243.

### Task 7 — Network Topology and PDF Export
The final task was to display the topology of the discovered network and save the result as a PDF.

After the scan was completed, I opened the Topology tab in Zenmap. The topology view visually displayed the discovered hosts within the scanned network, including 10.206.203.175 and 10.206.203.243.
<img width="1920" height="1040" alt="Task7-Zenmap-Network-Topology-2-Live-Hosts" src="https://github.com/user-attachments/assets/d1a1f0ec-a8aa-4c9f-aeb3-a88f52c75f5d" />

#### Task 7 Result
The network topology showing the discovered hosts was successfully displayed in Zenmap and saved as a PDF.

#### Network Topology PDF
The generated network topology PDF is included below as part of the project evidence.

[Task7-Zenmap-Network-Topology.pdf](https://github.com/user-attachments/files/32656788/Task7-Zenmap-Network-Topology.pdf)

---

### W2-PM5 Result
The Zenmap-based network scanning project was completed successfully. The local network configuration was identified, live hosts were discovered, their IP and MAC addresses were determined, and the resulting network topology was displayed and saved as a PDF.

### Challenges & Troubleshooting
Several issues were encountered during the Zenmap project and were resolved during the practical.

- Installer files transferred from another device produced NSIS integrity errors on the Windows PC.
- The installation succeeded after downloading the Nmap installer directly on the same Windows PC.
- The initial school Wi-Fi network used a /16 subnet, which created a much larger address space and caused the Zenmap scan to take significantly longer.
- During the school Wi-Fi scan, multiple IP addresses appeared with the same RouterBOARD MAC address, making the results difficult to interpret as separate physical hosts.
- To obtain clearer and more manageable results, the Windows PC was moved to a controlled mobile hotspot network using a /24 subnet.
- The network topology was preserved as a PDF using Microsoft Print to PDF.

These troubleshooting steps helped produce clearer and more manageable results for the remaining network discovery tasks.

### What I Learned
This practical helped me understand how Zenmap and Nmap can be used to discover hosts and examine devices within a network. I learned how to identify the local IPv4 address and subnet mask, determine the network size using CIDR notation, scan a subnet, and interpret the resulting host, IP address, MAC address, and topology information.

I also learned that the network environment can significantly affect scanning results. The difference between the school Wi-Fi /16 network and the mobile hotspot /24 network showed me how subnet size can affect the number of addresses being scanned and the time required to complete a scan.

The challenges encountered during the practical also improved my troubleshooting skills. Instead of bypassing installation errors or assuming unusual scan results were correct, I investigated the problems, changed the network environment where necessary, and verified the final results using different sources such as Zenmap and Windows network configuration.
