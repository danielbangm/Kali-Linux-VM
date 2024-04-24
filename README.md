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

I am going to head to the VMWare's site https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html to download VMWare Workstation 17 Pro for Windows and then start the installation process. It is a straightforward process from there, but here is a <a href="https://www.youtube.com/watch?v=7kcqDy7aeGg">Tutorial</a> on how to install VMWare step by step.
<p align="center">
<img src="https://shorturl.at/wABH2" />
</p>

-  Step 2: Download and Install Kali Linux

I am going to Download <a href="https://www.kali.org/get-kali/#kali-virtual-machines">Kali Linux</a> using the VMWare version and Install it on my local drive. Then use 7zip to extract file and launch the file with the ".vmx" extension with VMware 
![image](https://github.com/danielbangm/Kali-Linux-VM/assets/22795502/86cba444-734d-4c1f-9f05-b10484b5d971)
![image](https://github.com/danielbangm/Kali-Linux-VM/assets/22795502/a6fc32ac-a9b2-47f6-af76-cf74a6428857)

-  Step 3: Download and Install Metasploitable2

I am going to download the <a href="https://sourceforge.net/projects/metasploitable/files/Metasploitable2/">Metasploitable2 Zip file</a> and bring up the VMWare session but lauching the ".vmx" file extension with VMWare. This should start the Virtual Machine with Username: msfadmin and Password: msfadmin
![image](https://github.com/danielbangm/Kali-Linux-VM/assets/22795502/6cd638f3-ba76-4e06-a06f-d815bae30b71)

-  Step 4: Start OpenVAS

I will start the OpenVAS Process by bringing up a root console on Kali Linux and type the following command to start the services <b>gvm-start</b> . Then I change the password of the existing admin with the command <b>runuser-u _gvm -- gvmd --user=admin --new-password=admin</b>
![image](https://github.com/danielbangm/Kali-Linux-VM/assets/22795502/7377d224-a9b5-4bb1-ba00-e211f0bd163d)

- Step 5: Access OpenVAS

To access OpenVAS and take a look, just open up the Firefox Browser and go to the OpenVAS URL: https://127.0.0.1:9392
![image](https://github.com/danielbangm/Kali-Linux-VM/assets/22795502/7df7224c-621b-459b-a59f-7924f2af0de8)
Next login with the Username:admin, Password: admin
Once logged in, we see the main Dashboard view below: <b>Our initial Dashboard will be blank, because a Scan has not been run</b>
![image](https://github.com/danielbangm/Kali-Linux-VM/assets/22795502/06f6e4c9-e9a6-4f47-a980-0aec78c5fb29)
![image](https://github.com/danielbangm/Kali-Linux-VM/assets/22795502/64b86d8f-c6e2-40d9-8fa4-1b8f8b43574f)



