<p align="center">
<img src="https://shorturl.at/cjxy2" />
</p>

<h1>OpenVAS: Scanning Metasploitable2 - Prerequisites and Installation</h1>

The goal of this lab is to download and install Kali Linux virtual machine, Metasploitable2, OpenVAS using VMWare workstation and we will use later on to perform a vulnerability scan and come up with solutions for remediation.  

<h2>Objectives</h2>

-  Learning how to create virtual machine using VMWare Workstation
-  Installing OpenVAS on Kali Linux VM and Metasploitable2.
-  Gain a better understanding of all parts of OpenVAS (How to start and stop the OpenVAS process).

<h2>Environments and Technologies Used</h2>

- Virtual Machine
- Kali Linux VM
- OpenVAS
- VMWare Workstation
- Metasploitable2

<h2>Operating Systems Used</h2>

- Linux

<h2>List of Prerequisites</h2>

- You need to download VMWare Workstation and have a computer of at least 8GB of RAM

<h2>Installation steps</h2>

-  Step 1: Download and Install VMMWare Workstation

I am going to head to the VMWare's site https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html to download VMWare Workstation 17 Pro for Windows and then start the installation process. It is a straightforward process from there, but here is a <a href="https://www.youtube.com/watch?v=7kcqDy7aeGg">Tutorial</a>on how to install VMWare step by step.
![image](https://github.com/danielbangm/SIEM-ressources/assets/22795502/5af7cf61-58b6-4e5f-892c-d1b09dd2d9a2)
![image](https://github.com/danielbangm/SIEM-ressources/assets/22795502/ab5c4749-4849-4aed-be3c-b9ae132cbaaa)

-  Step 2: Set up Log Analytics workspaces

The purpose of this is to ingest logs from the Virtual Machine. We are going to ingest the Windows event logs and create our own custom logs that contains geographic information in order to discover where the attacker is coming from. To do that, just search for Log analytic workspaces on the portal and create one using the same ressource group. Then go on to Security center(Microsoft Defender for the Cloud) to enable the ability to gather logs from the virtual machine into the log analytic workspaces. Make sure to choose the log Analytics workspaces we just created and turn defender on and also data collection has to be set to "all". Finally go back to log Analytic workspaces and connect to the VM.
![image](https://github.com/danielbangm/SIEM-ressources/assets/22795502/b5ca8d9e-57b8-4be7-87bb-03140eb1a75c)

-  Step 3: Set up sentinel

We are going to use this as our SIEM to visualize the attack data. Just type azure sentinel in the search bar and create a new sentinel. Pick the log analytic workspaces we want to connect to oour logs.
![image](https://github.com/danielbangm/SIEM-ressources/assets/22795502/a4ed62a2-fa02-439a-a4df-b40116ebbec9)

-  Step 4: Connect to VM using Remote Desk Connection

Click on virtual machine in portal.azure and copy the public IP of the VM. Go on your desktop and launch remote desk Connection(Microsoft RDP) using the VM's public ip address , username and password we created earlier. and we have access to our virtual machine...
![image](https://github.com/danielbangm/SIEM-ressources/assets/22795502/e5fa5235-7e14-47f2-ae48-4a287af9e126)


