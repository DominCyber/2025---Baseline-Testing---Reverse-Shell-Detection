# 2025 - Baseline Testing - Reverse Shell Detection
## Summary
This reverse shell detection exercise is a baseline test to test fundamental cybersecurity concepts/skills as well as system and network operability.

### Consdierations
<p>-I DO NOT CONDONE THE USE OF OFFENSIVE MEANS OR TOOLS OUTSIDE OF A TESTING ENVIRONMENT</p>
<p>-Overall, this baseline test is meant to be a standard for an ever refined test environment to practice concepts, familiarize various red and blue team tool usage, and apply GRC and other cybersecurity administrative concepts.</p>
<p>-This test is formatted as a guide for air gapped-testing whenever necessary.</p>
<p>-This test has inspiration and is an adaptation of the exercise explored in: My DFIR - Cybersecurity Tip: Build A Basic Home Lab (3/3) - https://www.youtube.com/watch?v=-8X7Ay4YCoA</p>
<p>-The entire test is conducted within a closed VMware hypervisor environment, with three virtual machines; an attacker Kali Linux, a target Windows Server 2019, and a monitoring Windows 10.</p>
<p>-The Windows Server 2019 has been configured to have its firewall and real-time antivirus turned off to allow for malware proof-of-concept deployment.</p>
<p>-Wireshark is used on the Windows 10 machine is used to monitor the Eth0 virtual adapter for traffic to and from the attacking and targeting virtual machines.</p>

### Tools/Applications Used
<p>-VMware hypervisor</p>
<p>--Virtual Machine OS</p>
<p>---Kali Linux</p>
<p>----Nmap CLI</p>
<p>----Metasploit CLI</p>
<p>----Python3 script</p>
<p>---Windows Server 2019</p>
<p>---Windows 10</p>
<p>----Wireshark</p>
<p>----Windows CLI</p>






### Steps
<img src="https://i.imgur.com/jMzVO1j.png" style="width: 100%;" alt="1">
<p><i>Ref 1: Discovering interfaces to conduct packet capture</i></p>
<img src="https://i.imgur.com/odnHQjg.png" style="width: 200%;" alt="1">
<p><i>Ref 2: Interface, port, number of captures, and export file designated, while script is prompted to run in the background and not resolving names, simlariy website opening and export .pcap information is displayed </i></p>
<img src="https://i.imgur.com/UJcMTKy.png" style="width: 100%;" alt="1">
<p><i>Ref 3: Export file read with verbose option</i></p>
<p><b>Significant takeaways for the packet header information:</b></p>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

<table border="1">
  <tr>
    <th>Element</th>
    <th>Examples</th>
    <th>Examples</th>
    <th>Examples</th>
    <th>Examples</th>
  </tr>
 <tr>
    <td>TTL</td>
    <td>64 (Linux)</td>
    <td>126 (128 is Windows)</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>TOS</td>
    <td>0x0 (default)</td>
    <td>0x60 (CS3)*</td>
    <td>0x80 (CS4)**</td>
    <td></td>
  </tr>
  <tr>
    <td>Flags</td>
    <td>[P.] (Push data)</td>
    <td>[.] (ACK)</td>
    <td>[S.] (SYN/ACK)</td>
    <td>[F.] (FIN/ACK)</td>

  </tr>
</table>

</body>
</html>
<p><i>*CS3 class selector 3; broadcast video</i> (1)</p)>
<p><i>**CS4 class selector 4; real-time interactive</i> (1)</p>
<img src="https://i.imgur.com/bcsBpDP.png" style="width: 100%;" alt="1">
<p><i>Ref 4: Hexadecimal and ASCII code is generated to view for anomalies </i></p>

### References
(1) Configuration Guidelines for DiffServ Service Classes. https://datatracker.ietf.org/doc/html/rfc4594.
