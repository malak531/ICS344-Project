# ICS344 Cybersecurity Project

**Group Number:** 3  
**Course:** ICS344  
**Project Topic:** Attacking and Defending a Metasploitable3 Machine

## Group Members

- **Malak Kamaleldin** – `202185450`  
- **Salma Salem** – `202185390`

---

## Task Distribution
The tasks were distributed very equally. We used team meetings to work on all the phases together. 

| Name              | Tasks Completed                                   |
|-------------------|---------------------------------------------------|
| Malak  | Phase 1, Phase 2, Phase 3, README writing, Uploading to Github  |
| Salma       |Virtual Machine Set Up, Phase 1, Phase 2, Phase 3, Screenshot Collection  |

---
## Project Overview

This project aims to simulate a **real-world cyberattack** on a vulnerable machine (Metasploitable3) and **analyze the attack using SIEM** tools. Additionally, we propose and test a **defensive strategy** to protect against similar future attacks.

---

## Phase 1: Environment Setup & Initial Attack

### Environment Setup

- **Victim Machine:** Metasploitable3  
- **Attacker Machine:** Kali Linux (attacking using Metasploit)  
- **Virtualization Platform:** UTM & VirtualBox (as needed)

### Objective

Gain unauthorized access to the Metasploitable3 machine by performing a **manual SSH brute-force attack** using lists of common usernames and passwords. We also used a custom Python script to attack the victim machine.  


---

## Phase 2: Visual Analysis with a SIEM Dashboard

### Objective

After successfully compromising the victim machine, the next step was to **monitor and visualize the attack data**. We installed Splunk on the attacker machine and forwarded log data from the victim machine using Splunk's monitoring tools.

### Tools and Configuration

- **SIEM Tool:** Splunk Enterprise
- **Forwarded Logs:** `/var/log/auth.log` from the victim machine
- **Monitoring Goal:** Identify successful and failed login attempts, analyze attack frequency, and visualize brute-force attempts.

### Outcome

We created dashboards on Splunk to display authentication logs, showing both **successful breaches and failed login attempts**. Visualization included bar charts of accepted vs. failed attempts, which helped identify patterns of brute-force activity.

---

## Phase 3: Defense & Prevention

### Objective

To defend against further attacks, we implemented **Fail2Ban**, a log-parsing security tool that protects servers against brute-force attacks by banning IPs after multiple failed login attempts.

### Defensive Measures

- **Tool Used:** Fail2Ban
- **Monitored Logs:** `/var/log/auth.log`
- **Configured Settings:**
  - Max Retry Attempts: `3`
  - Ban Time: `6000` seconds (1 hour and 40 minutes)

### Outcome

Fail2Ban successfully identified repeated brute-force attempts and temporarily banned offending IP addresses. We validated this by checking logs and ensuring further login attempts from banned sources were rejected.

---







