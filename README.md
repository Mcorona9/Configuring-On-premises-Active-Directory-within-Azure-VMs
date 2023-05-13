# Configuring-On-premises-Active-Directory-within-Azure-VMs

<p>
<img src="https://i.imgur.com/2oMXnpT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Various Command-Line Tools



<h2>Operating Systems Used </h2>

- Windows 10 (21H2)



<p>
<img src="https://i.imgur.com/JfZE9ed.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this lab, we will create two VMs in the same VNET: a Domain Controller and a Client machine. The Domain Controller will offer Active Directory services to the Client machine, so we will assign it a static IP. Additionally, we will join the Client machine to the domain.
</p>
<br />



<p>
<img src="https://i.imgur.com/tHTcq6M.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
DC-1 needs to have a static Private IP Address. Client-1 will connect to DC-1, but initially, the ping between them will not work correctly. To ensure connectivity, we need to enable ICMPv4 on the firewall of DC-1. After enabling ICMPv4, we can successfully ping DC-1 from Client-1
</p>
<br />

<p>
<img src="https://i.imgur.com/xpd1EoX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The screenshot above confirms that after enabling ICMPv4 on the firewall, we now have successful connectivity.
</p>
<br />

<p>
<img src="https://i.imgur.com/jEHDGyt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We can now start the process of installing active directory on the client 1 machine as shown above. 
</p>
<br />

<p>
<img src="https://i.imgur.com/GrSr2mn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Using the our domain credentials we will loging to the client-1 machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/y3HYotR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, we have started a continuous ping by using the "-t" command and specifying the private IP address of VM2. The purpose of this step is to ensure a constant flow of traffic between the two virtual machines, which will aid in our troubleshooting efforts. In the next step, we will be modifying the firewall settings of VM2 to block incoming traffic using the ICMP protocol. Specifically, we will be preventing any new ping requests from being initiated towards VM2. This will allow us to test the effectiveness of the firewall settings and ensure that incoming traffic is being blocked as intended.
</p>
<br />

<p>
<img src="https://i.imgur.com/1Umkdmk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After modifying the firewall settings in VM2 to block incoming traffic using the ICMP protocol, we can now observe that the continuous ping from VM1 has come to a stop. This confirms that the firewall is functioning as intended, and incoming traffic using the specified protocol is now being blocked. This is a critical step in ensuring the security and integrity of our virtual environment and protecting it against potential threats and vulnerabilities. By successfully blocking incoming traffic, we can safeguard our network and data from malicious attacks and unauthorized access. With the firewall settings in place, we can continue our exploration of the virtual environment with greater confidence and peace of mind.
</p>
<br />

<p>
<img src="https://i.imgur.com/a8F3lAO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, we will be using the SSH command in PowerShell to establish a remote connection to VM2 from VM1. This will allow us to access and modify the settings and configurations of VM2 from a remote location. SSH is a secure protocol that provides encrypted communication between two systems, making it an ideal choice for remote access and administration. 
</p>
<br />

<p>
<img src="https://i.imgur.com/qSyVkgh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, we will be using the SSH command in PowerShell to establish a remote connection to VM2 from VM1. This will allow us to access and modify the settings and configurations of VM2 from a remote location. SSH is a secure protocol that provides encrypted communication between two systems, making it an ideal choice for remote access and administration. 
</p>
<br />

<p>
<img src="https://i.imgur.com/RVDbFNn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, we will be using the SSH command in PowerShell to establish a remote connection to VM2 from VM1. This will allow us to access and modify the settings and configurations of VM2 from a remote location. SSH is a secure protocol that provides encrypted communication between two systems, making it an ideal choice for remote access and administration. 
</p>
<br />

<p>
<img src="g]https://i.imgur.com/zX4HUmi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, we will be using the SSH command in PowerShell to establish a remote connection to VM2 from VM1. This will allow us to access and modify the settings and configurations of VM2 from a remote location. SSH is a secure protocol that provides encrypted communication between two systems, making it an ideal choice for remote access and administration. 
</p>
<br />

<p>
<img src="https://i.imgur.com/zX4HUmi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, we will be using the SSH command in PowerShell to establish a remote connection to VM2 from VM1. This will allow us to access and modify the settings and configurations of VM2 from a remote location. SSH is a secure protocol that provides encrypted communication between two systems, making it an ideal choice for remote access and administration. 
</p>
<br />

<p>
<img src="https://i.imgur.com/Xlr0r04.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, we will be using the SSH command in PowerShell to establish a remote connection to VM2 from VM1. This will allow us to access and modify the settings and configurations of VM2 from a remote location. SSH is a secure protocol that provides encrypted communication between two systems, making it an ideal choice for remote access and administration. 
</p>
<br />


<p>
<img src="https://i.imgur.com/Ks2Mhlw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, we will be using the SSH command in PowerShell to establish a remote connection to VM2 from VM1. This will allow us to access and modify the settings and configurations of VM2 from a remote location. SSH is a secure protocol that provides encrypted communication between two systems, making it an ideal choice for remote access and administration. 
</p>
<br />

<p>
<img src="https://i.imgur.com/NDoQwU3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, we will be using the SSH command in PowerShell to establish a remote connection to VM2 from VM1. This will allow us to access and modify the settings and configurations of VM2 from a remote location. SSH is a secure protocol that provides encrypted communication between two systems, making it an ideal choice for remote access and administration. 
</p>
<br />

<p>
<img src="https://i.imgur.com/s0PaZAy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, we will be using the SSH command in PowerShell to establish a remote connection to VM2 from VM1. This will allow us to access and modify the settings and configurations of VM2 from a remote location. SSH is a secure protocol that provides encrypted communication between two systems, making it an ideal choice for remote access and administration. 
</p>
<br />

<p>
<img src="https://i.imgur.com/4dCZ48E.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, we will be using the SSH command in PowerShell to establish a remote connection to VM2 from VM1. This will allow us to access and modify the settings and configurations of VM2 from a remote location. SSH is a secure protocol that provides encrypted communication between two systems, making it an ideal choice for remote access and administration. 
</p>
<br />






