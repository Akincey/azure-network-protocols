<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create sample files with various permissions
- Create a Security Group
- Assign permissions
- Attempt to access accounts

<h2>Actions and Observations</h2>

<p>

![image](https://github.com/user-attachments/assets/3109e446-832e-4f7f-ab70-1a69755e71a0)

</p>
<p>
In this step, I am creating a Group Policy Object (GPO) designed to apply uniform configurations and security settings across all client machines within the domain. This ensures centralized management and helps maintain consistency, compliance, and control throughout the networked environment.
</p>
<br />


![image](https://github.com/user-attachments/assets/418b288c-9e7f-4647-8059-d8b2bdd16995)


</p>
<p>
In this step, I am using the Group Policy Management Console to implement an account lockout policy. This includes configuring the lockout duration, threshold for invalid login attempts, and the reset time. The goal is to enhance security by mitigating the risk of brute-force attacks while maintaining usability for domain users.
</p>
<br />

<p>

 ![image](https://github.com/user-attachments/assets/3e40cd35-6652-46cb-890b-f76781f3a601)
 
</p>
<p>
After the virtual machine received the newly applied Group Policy, I used the Command Prompt with gpupdate /force to manually refresh the policy settings. I then verified successful application by running gpresult /r, confirming that the updated Group Policy had been correctly enforced on the system.
</p>
<br />
