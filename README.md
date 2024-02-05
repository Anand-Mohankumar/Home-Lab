# Home-Lab for Purple Teaming Activities

Welcome to the Purple Teaming Home Lab Project! This initiative is designed to guide security enthusiasts, professionals, and learners in setting up a practical and effective purple teaming environment within the confines of their home lab. Purple teaming is a collaborative approach to security testing, bringing together both offensive (red team) and defensive (blue team) strategies to enhance overall cybersecurity resilience.

## Project Goals:


### Hands-on Learning : 
- Provide a comprehensive guide for creating a purple teaming home lab that facilitates practical, real-world experience in offensive and defensive security techniques.

### Skill Development :
- Equip users with the skills necessary to simulate and assess security threats, vulnerabilities, and incidents in a controlled environment.


## Requirements :

> Spoiler alert!! You're going to need a capable host machine to successfully run this lab. But If your system is struggling, we still have the option to run only specific parts of the architecture at a time and still achieve the same result. 
> <br> </br>


- ***Oracle Virtualbox*** : Can be downloaded [**here**](https://www.virtualbox.org/wiki/Downloads).
- ***Windows Host System***
    - This is where we'll be installing our Hypervisor
    - Recommended specs :
      - Processor with 6 Cores (12 Threads)
      - 16 GB RAM
      - HDD - 100 GB
- ***Windows Server 2022***
- ***Windows 10 Enterprise***
  -  You can also try 11, but if you're short on resources, personally I think 10 is the sweet spot
- ***Ubuntu 22.04***
- ***Kali Linux***
  - You can utilize the ready to use version for Virtualbox.
  
- ***Wazuh***
  - You can utilize the ready to use version for Virtualbox or Install from scratch (which is time consuming but if your objective is to learn, why not?).
- ***pfSense***
- ***Suricata***

## Lab Architecture :

![Purple Team Lab Architecture](/PurpleTeam_Lab_Architecture.png)

<center>Lab Setup Architecture</center>


 #### Since this is quite complicated of a setup, I've broken down the whole thing into multiple parts. We'll go through each of them seperately. Use the links below to get to a specific part of the implementation.
---
## Lab Architecture Breakdown

|No|Section|Description|
|:-----:|:-----:|:----:|
|1|[pfSense](/pfSense/pfSense%20Setup.md)|Installiing pfSense Router software and Integrating Suricata IDS/IPS
|2|[Active Directory](/Active%20Directory/Active%20Directory%20Setup.md)|Setup Active Directory in Windows Server 2022|
|3|[Endpoints](/Endpoints/Endpoint%20Setup.md)|Fresh install Operating Systems domain joined to AD|
|4|[Lima Charlie](/Lima%20Charlie/LimaCharlie%20Setup.md)|Create Account in LimaCharlie, Install LC agent on Endpoint|
|5|[Wazuh](/Wazuh/Wazuh%20Setup.md)|Install Wazuh, Install Wazuh Agent on Endpoint|

>Note : The sections of the setup is placed sequenctially to reduce the effort as much as possible. Kindly follow the sequence fom 1-5 unless otherwise you have a valid reason.
---
