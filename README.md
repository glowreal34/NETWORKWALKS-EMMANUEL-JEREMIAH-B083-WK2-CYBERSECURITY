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
