# 2025 - Baseline Testing - Reverse Shell Detection
## Summary
This reverse shell detection exercise is a baseline test to test fundamental cybersecurity concepts/skills as well as system and network operability.

### Consdierations
<p>-I DO NOT CONDONE THE USE OF OFFENSIVE MEANS OR TOOLS OUTSIDE OF A TESTING ENVIRONMENT</p>
<p>-Overall, this baseline test is meant to be a standard for an ever refined test environment to practice concepts, familiarize various red and blue team tool usage, and apply GRC and other cybersecurity administrative concepts.</p>
<p>-This test is formatted as a guide for air gapped-testing whenever necessary.</p>
<p>-This test has inspiration and is an adaptation of the exercise explored in: MyDFIR - Cybersecurity Tip: Build A Basic Home Lab (3/3) - https://www.youtube.com/watch?v=-8X7Ay4YCoA</p>
<p>-The entire test is conducted within a closed VMware hypervisor environment, with three virtual machines; an attacker Kali Linux, a target Windows Server 2019, and a monitoring Windows 10.</p>
<p>-The Windows Server 2019 has been configured to have its firewall and real-time antivirus turned off to allow for malware proof-of-concept deployment.</p>
<p>-It is assumed that a would-be attacker has applied various techniques to cause a user to open the remote executable, allowing for reverse shell execution. Additionally, it's assumed there has been no log tampering.</p>
<p>-Wireshark is used on the Windows 10 machine is used to monitor the Eth0 virtual adapter for traffic to and from the attacking and targeting virtual machines.</p>

### Tools/Applications Used
#### VMware hypervisor on a Lenovo Thinkbook 16 G6
##### Virtual Machine OS
<p>-Kali Linux</p>
<p>--Nmap CLI</p>
<p>--Metasploit CLI</p>
<p>--Python3 script (for HTTP listening session)</p>
<p>-Windows Server 2019</p>
<p>-Windows 10</p>
<p>--Wireshark</p>
<p>--Windows CLI</p>

### Concepts/Skills demonstrated 
#### Concepts
<p>-Networking architecture, ports, and protocols</p>
<p>-System operability</p>
<p>-Log aggregation</p>
<p>-Cyber kill chain procedures</p>
<p>--Reconnaissance</p>
<p>--Weaponization</p>
<p>--Delivery</p>

#### Skills
##### Blue Team
<p>-Log Aggregation - Wireshark recordings</p>
<p>-Log Aggregation - Windows CLI - Process ID for network activity</p>
<p>-Log Aggregation - Task Manager - Process ID for network activity</p>

##### Red Team
<p>-Reconnaissance - enumerating target VM's ports</p>
<p>-Weaponization - Metasploit payload</p>
<p>-Weaponization - Metasploit console configuration</p>
<p>-Delivery - via web application</p>

### Timeline
<img src="https://i.imgur.com/gAoZtoF.png" style="width: 50%;" alt="1">
<p><i>Ref 1: Testing connectivity between virtual machines</i></p>
<img src="https://i.imgur.com/n5KHrVM.png" style="width: 200%;" alt="1">
<p><i>Ref 2: Log Aggregation - Wireshark recordings (ICMP ping execution)</i></p>
<img src="https://i.imgur.com/rwtrdeZ.png" style="width: 75%;" alt="1">
<p><i>Ref 3: Reconnaissance - enumerating target VM's ports</i></p>
<img src="https://i.imgur.com/zzPxg0o.png" style="width: 100%;" alt="1">
<p><i>Ref 4: Log Aggregation - Wireshark logs (Nmap execution)</i></p>
<img src="https://i.imgur.com/XqWwOjs.png" style="width: 75%;" alt="1">
<p><i>Ref 5: Weaponization - Metasploit payload</i></p>
<img src="https://i.imgur.com/hXt7M0X.png" style="width: 100%;" alt="1">
<p><i>Ref 6: Weaponization - Metasploit console configuration</i></p>
<img src="https://i.imgur.com/A4xDL0u.png" style="width: 100%;" alt="1">
<p><i>Ref 7: Delivery - via web application</i></p>
<img src="https://i.imgur.com/nr0FstW.png" style="width: 100%;" alt="1">
<p><i>Ref 8: Log Aggregation Wireshark - Windows CLI - Task Manager - Process ID for network activity</i></p>
