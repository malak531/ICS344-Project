# Phase 1: Compromise SSH Service on Metasploitable3 using Metasploit

## 🔁 Connectivity Verification

Before running any attack, we ensured both machines could communicate over the network.

### Ping from Attacker (Kali) to Victim (Metasploitable3) (the IP address was then changed to 10.0.2.7):
```bash
ping 10.0.2.5
```
### Ping from Victim to Attacker :
```bash
ping 10.0.2.15
