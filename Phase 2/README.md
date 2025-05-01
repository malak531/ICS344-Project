# Phase 2: Visual Analysis with a SIEM Dashboard

## Objective

Use a SIEM platform to collect and visualize data from the victim and the honeypot environments.

###  Forwarding the Server 

```bash
sudo /opt/splunk/bin/splunk add forward-server 10.0.2.15:9997
sudo /opt/splunk/bin/splunk add monitor /var/log/auth.log

```
![Alt Text](Fowarding_The_Server.png)

### Log From The Victim Server
This is the /user/log/auth.log file on the victim machine, which is being forwarded to Splunk on the attacker machine. 

```bash
sudo cat /user/log/auth.log

```
![Alt Text](sudo_cat.png)















