# Home-Lab for Purple Teaming Activities

Welcome to the Purple Teaming Home Lab Project!

 This project is designed to guide security enthusiasts, professionals, and learners in setting up a practical and effective purple teaming environment within the confines of their home lab.
### What is Purple Teaming?  
Purple teaming is a collaborative approach to security testing, bringing together both offensive (red team) and defensive (blue team) strategies to enhance overall cybersecurity resilience.

## Project Goals:


### Hands-on Learning : 
- Provide a comprehensive guide for creating a purple teaming home lab that facilitates practical, real-world experience in offensive and defensive security techniques.

### Skill Development :
- Equip users with the skills necessary to simulate and assess security threats, vulnerabilities, and incidents in a controlled environment.

## Lab Requirements :

> Spoiler alert!! You're going to need a capable host machine to successfully run this lab.  
> But If your system is struggling, we still have the option to run only specific parts of the architecture at a time and still achieve the same result. 
> <br> </br>



- ***Windows Host System***
    - This is where we'll be installing our Hypervisor
    - Recommended specs :
      - Processor with 6 Cores (12 Threads)
      - 16 GB RAM
      - HDD - 250 GB free


- ***Oracle Virtualbox*** : Can be downloaded [***here***](https://www.virtualbox.org/wiki/Downloads).  

  > Note: Installation procedure for Virtualbox is not covered in this guide. But here's a link to the official documentation from Oracle if you have trouble installing the software : [***1.5. Installing Oracle VM Virtualbox and Extension Packs***](https://www.virtualbox.org/manual/UserManual.html#installation)


- ***Windows Server 2022***
  - ISO image can be downloaded from [***here***](https://info.microsoft.com/ww-landing-windows-server-2022.html)
  >Note : Microsoft requires you to register in order to dowload the ISO file.


- ***Windows 10 Enterprise***
  -  ISO image available [***here***](https://www.microsoft.com/en-us/evalcenter/download-windows-10-enterprise)
  -  You can also try 11, but if you're short on resources, personally I think 10 is the sweet spot.
 

- ***Kali Linux***
  - You can utilize the ready to use version for Virtualbox available [***here***](https://www.kali.org/get-kali/#kali-virtual-machines)
  - In the **Pre-built Virtual Machines** section, download the package for Virtualbox

  >Note : Virtual Machine package typically comes in a compressed archive format. Hence, if the Windows explorer fails to extract the package, keep third party tool such as 7zip or Winrar in your host system just in case.
  
- ***Wazuh***
  - You can utilize the ready to use version for Virtualbox or Install from scratch (which is time consuming but if your objective is to learn, why not?).

  - Virtual machine (OVA) for easy installation to Virtualbox can be found [***here***](https://documentation.wazuh.com/current/deployment-options/virtual-machine/virtual-machine.html)

  - If you'd like to install Wazuh by other means, refer : [***Installation alternatives***](https://documentation.wazuh.com/current/deployment-options/index.html)

- ***pfSense***
  - Visit : [***Download pfSense Community Edition***](https://www.pfsense.org/download/)
  - In the **Select Image to Download** section, select the following and click Download.
  >|Architecture|Installer|Mirror
  >|----|----|----|
  >|AMD64(64-bit)|DVD Image (ISO)Installer|Choose your nearest location|

- ***Suricata***

## Lab Architecture :

![Purple Team Lab Architecture](/PurpleTeam_Lab_Architecture.png)

<center>Lab Setup Architecture</center>


 #### Since this is quite complicated of a setup, I've broken down the whole thing into multiple parts. We'll go through each of them seperately. Use the links below to get to a specific part of the implementation.
---
## Getting Started


### Part 1. Getting things Up and Running


The setup has a few building blocks and the below table has detailed description on how to get each of them up and running and connected with each other.


|No|Section|Description|
|:-----:|:-----:|:----:|
|1|[pfSense](/pfSense/pfSense%20Setup.md)|Installiing pfSense Router software and Integrating Suricata IDS/IPS
|2|[Active Directory](/Active%20Directory/Active%20Directory%20Setup.md)|Setup Active Directory in Windows Server 2022|
|3|[Endpoints](/Endpoints/Endpoint%20Setup.md)|Fresh install Operating Systems domain joined to AD|
|4|[Lima Charlie](/Lima%20Charlie/LimaCharlie%20Setup.md)|Create Account in LimaCharlie, Install LC agent on Endpoint|
|5|[Wazuh](/Wazuh/Wazuh%20Setup.md)|Install Wazuh, Install Wazuh Agent on Endpoint|

>Note : The sections of the setup is placed sequenctially to reduce the effort as much as possible. Kindly follow the sequence fom 1-5 unless otherwise you have a valid reason.
---
### Part 2. Practicing


This is part where we really touch on our actual objective of the lab. With all the monitoring and defensive tools and our environment fully set up, now its time to start practicing. 

In this part of the lab we use the Kali Linux to try out various redteaming tools against our defensive arsenal to observe how they perform.

|No|CaseID |Description|
|:-----:|:-----:|:----:|