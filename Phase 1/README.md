# Phase 1: Compromise SSH Service on Metasploitable3 using Metasploit

## Task 1.1: Use Kali Linux tool Metasploit to compromise the service.
### Connectivity Verification

Before running any attack, we checked the IP address of both machines and ensured they could communicate over the network without issues.
### IP Address of Attacker Machine (Kali):
```bash
ip a
```
![Alt Text](Attacker_Machine_IPAddress.png)


### IP Address of Victim Machine (Metasploitable3):
```bash
ip a
```
![Alt Text](Victim_Machine_IPAddress.png)


### Ping from Attacker to Victim:
```bash
ping 10.0.2.15
```
![Alt Text](Ping_From_Attacker.png)


### Ping from Victim to Attacker:
```bash
ping 10.0.2.7
```
![Alt Text](Ping_From_Victim.png)


### Start Attack from Attacker Machine :
This attack will be an SSH brute force attack to find the login credentials of the victim machine. The rest of the commands are found in the screenshot below. 
```bash
msfconsole
```
![Alt Text](Mfsconsole.png)
![Alt Text](Command_To_Start_Attack.png)

### Find Successful Credentials :
The brute force attack finds that vagrant: vagrant is a match. 

![Alt Text](Brute_Force_Attack_On_Victim_Machine.png)

### The Session Between the Machines is Opened :

![Alt Text](Active_Sessions_On_Attacker_Machine.png)



## Task 1.2: Compromise the service using a custom script that you create

### The Custom Python Script :
This custom Python script tries to open a session with the victim machine. 

![Small Image](Custom_Program_Script.png)


### Running the Python Script on Attacker Machine: 

![Alt Text](Running_The_Custom_Script.png)












