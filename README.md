# Footprinting and Reconnaissance Using Kali Linux Tools

## Project Overview

This project explores the fundamental concepts of cybersecurity footprinting and reconnaissance through the practical use of six command-line tools available in Kali Linux.

Footprinting is an information-gathering process used during the initial stages of security assessments. It helps security professionals understand a target organisation's publicly available digital infrastructure, domain information, web technologies and DNS configuration.

The practical exercises demonstrate how different reconnaissance tools can be used to collect and analyse publicly accessible technical information.

## Objectives

- Understand the role of footprinting and reconnaissance in cybersecurity.
- Investigate publicly available domain registration information.
- Identify technologies used by a target website.
- Understand DNS resolution and record enumeration.
- Examine HTTP response headers.
- Identify the presence of Web Application Firewall (WAF) technologies.
- Understand how reconnaissance findings contribute to security assessments.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| WHOIS | Retrieves publicly available domain registration information. |
| WhatWeb | Identifies web technologies and server-related information. |
| NSLookup | Performs DNS queries and domain name resolution. |
| cURL | Retrieves HTTP response headers. |
| WAFW00F | Identifies potential Web Application Firewall technologies. |
| DNSRecon | Performs DNS enumeration and identifies available DNS records. |
| Kali Linux | Linux distribution used for cybersecurity and penetration-testing exercises. |

## Practical Tasks

### Task 01 – Domain Registration Information Using WHOIS

**Command:**
```bash
whois networkwalks.com
```

**Objective:**

Retrieve publicly available domain registration information, including registrar details, registration dates and name servers.

**Methodology:**

The WHOIS utility was executed against the authorised target domain. The returned information was examined to understand the domain's registration and administrative details.

**Key Learning:**

WHOIS provides useful information about domain ownership records, registration details and DNS infrastructure. This information can help security professionals understand an organisation's external digital footprint.

**Evidence:**

Screenshot: `screenshots/01-whois.png`

---

### Task 02 – Web Technology Fingerprinting Using WhatWeb

**Command:**
```bash
whatweb networkwalks.com
```

**Objective:**

Identify publicly detectable technologies and components associated with the target website.

**Methodology:**

WhatWeb was used to examine the website and identify detectable technologies, server information and other available web-related details.

**Key Learning:**

Technology fingerprinting helps security professionals understand the technologies exposed by a web application. Identifying software components can support vulnerability assessment and security hardening activities.

**Evidence:**

Screenshot: `screenshots/02-whatweb.png`

---

### Task 03 – DNS Resolution Using NSLookup

**Command:**
```bash
nslookup networkwalks.com
```

**Objective:**

Understand how a domain name is resolved through the Domain Name System (DNS).

**Methodology:**

NSLookup was executed to query DNS information associated with the target domain. The returned response was examined to understand domain resolution.

**Key Learning:**

DNS resolution translates human-readable domain names into IP addresses. Understanding this process is essential for network troubleshooting, infrastructure analysis and cybersecurity assessments.

**Evidence:**

Screenshot: `screenshots/03-nslookup.png`

---

### Task 04 – HTTP Response Header Analysis Using cURL

**Command:**
```bash
curl -I https://networkwalks.com
```

**Objective:**

Examine HTTP response headers returned by the target website.

**Methodology:**

The cURL utility was used with the `-I` option to retrieve HTTP response headers without downloading the complete webpage. The returned headers were examined for available server, status and response-related information.

**Key Learning:**

HTTP response headers provide valuable information about how a web server communicates with clients. Reviewing these headers can help identify potential information disclosures and opportunities to improve security configurations.

**Evidence:**

Screenshot: `screenshots/04-curl-headers.png`

---

### Task 05 – Web Application Firewall Detection Using WAFW00F

**Command:**
```bash
wafw00f networkwalks.com
```

**Objective:**

Investigate whether a Web Application Firewall (WAF) is detectable in front of the target website.

**Methodology:**

WAFW00F was executed to analyse the website's responses and identify indicators associated with Web Application Firewall technologies.

**Key Learning:**

A Web Application Firewall helps protect web applications by monitoring and filtering HTTP traffic. Understanding WAF detection techniques provides insight into the defensive technologies used to protect web-facing services.

**Evidence:**

Screenshot: `screenshots/05-wafw00f.png`

---

### Task 06 – DNS Enumeration Using DNSRecon

**Command:**
```bash
dnsrecon -d networkwalks.com
```

**Objective:**

Perform DNS enumeration to identify publicly available DNS records associated with the target domain.

**Methodology:**

DNSRecon was used to query the target domain and examine the DNS information returned by the tool. The results were reviewed to understand the domain's publicly exposed DNS configuration.

**Key Learning:**

DNS enumeration helps security professionals understand an organisation's DNS infrastructure, including available name server, mail server and other DNS records.

**Evidence:**

Screenshot: `screenshots/06-dnsrecon.png`

---

## Key Findings and Observations

The practical exercises demonstrated how multiple reconnaissance tools can be combined to develop an overview of an organisation's publicly accessible digital infrastructure.

Each tool provided a different perspective:

- WHOIS provided domain registration information.
- WhatWeb identified detectable web technologies.
- NSLookup demonstrated domain name resolution.
- cURL provided insight into HTTP response headers.
- WAFW00F demonstrated WAF detection techniques.
- DNSRecon provided information about publicly available DNS records.

The combined results illustrate why reconnaissance is an important preliminary activity in cybersecurity assessments.

## Conclusion

This practical project provided hands-on experience with six widely used reconnaissance tools in Kali Linux.

Through these exercises, I developed a better understanding of domain information gathering, web technology fingerprinting, DNS analysis, HTTP header inspection and Web Application Firewall detection.

The project strengthened my practical knowledge of the reconnaissance phase of ethical hacking and demonstrated how publicly available technical information can be analysed to understand an organisation's external attack surface.

## Ethical Considerations

All activities were performed for educational purposes within the scope of the assigned cybersecurity practical.

Reconnaissance activities should only be conducted against systems and domains for which appropriate authorisation has been obtained. Information gathered during security assessments should be handled responsibly and must not be used for unauthorised access or malicious activities.

---

**Project:** W2-PM1 – Week 2 Project Module 1  
**Domain used in the practical:** `networkwalks.com`  
**Environment:** Kali Linux  
**Category:** Cybersecurity | Ethical Hacking | Footprinting & Reconnaissance
