2025 - Baseline Testing - Reverse Shell Detection

Summary
This reverse shell detection exercise is a baseline test to test fundamental cybersecurity concepts/skills as well as system and network operability.

Considerations
-I DO NOT CONDONE THE USE OF OFFENSIVE MEANS OR TOOLS OUTSIDE OF A TESTING ENVIRONMENT

-Overall, this baseline test is meant to be a standard for an ever refined test environment to practice concepts, familiarize various red and blue team tool usage, and apply GRC and other cybersecurity administrative concepts.

-This test is formatted as a guide for air gapped-testing whenever necessary.

-This test has inspiration and is an adaptation of the exercise explored in: My DFIR - Cybersecurity Tip: Build A Basic Home Lab (3/3) - https://www.youtube.com/watch?v=-8X7Ay4YCoA

-The entire test is conducted within a closed VMware hypervisor environment, with three virtual machines; an attacker Kali Linux, a target Windows Server 2019, and a monitoring Windows 10.

-The Windows Server 2019 has been configured to have its firewall and real-time antivirus turned off to allow for malware proof-of-concept deployment.

-Wireshark is used on the Windows 10 machine is used to monitor the Eth0 virtual adapter for traffic to and from the attacking and targeting virtual machines.

Tools/Applications Used
-VMware hypervisor
-network architecture construction

--Virtual Machine OS 
---Kali Linux
----Nmap CLI
----Metasploit CLI
----Python3 script
---Windows Server 2019 
---Windows 10
----Wireshark
----Windows CLI

Concepts/Skills demonstrated 
-Concepts
-Networking architecture, ports, and protocols
-system operability
-Log aggregation
-Cyber kill chain procedures
--Reconnaissance
--Weaponization
--Delivery

-Skills
--Blue Team
---Log Aggregation - Wireshark recordings
---Log Aggregation - Windows CLI - Process ID for network activity
---Log Aggregation - Task Manager - Process ID for network activity

--Red Team
---Reconnaissance - enumerating target VM's ports
---Weaponization - Metasploit payload
---Weaponization - Metasploit console configuration
---Delivery - via web application 

Timeline

Testing connectivity between virtual machines

Log Aggregation - Wireshark recordings

Reconnaissance - enumerating target VM's ports

Log Aggregation - Wireshark recordings

Weaponization - Metasploit payload

Weaponization - Metasploit console configuration

Delivery - via web application 

Log Aggregation - Wireshark - Windows CLI - Task Manager - Process ID for network activity




