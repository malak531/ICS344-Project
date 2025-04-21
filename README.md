# ICS344 Cybersecurity Project

**Group Number:** 3  
**Course:** ICS344  
**Project Topic:** Attacking and Defending a Metasploitable3 Machine

## Group Members

- **Malak Kamaleldin** – `202185450`  
- **Salma Salem** – `202185390`

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

We targeted the **HTTP service** hosted on Metasploitable3, specifically a vulnerable instance of **Apache Tomcat**.

### Approach

- Identify open ports and services using tools like `nmap`.
- Target the Apache Tomcat Manager application on port `8180`.
- Use **Metasploit Framework** to exploit the service and gain remote access.

---

