# Configuring-On-premises-Active-Directory-within-Azure-VMs

<p>
<img src="https://i.imgur.com/2oMXnpT.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
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
The image above illustrates us logging into our DC-1 vm and starting the process of installing Active Directory domain services and soon after promoting it as our Domain controller.
</p>
<br />

<p>
<img src="https://i.imgur.com/GrSr2mn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After restarting DC-1 we will now log back into the now converted domain controller using the our domain credentials that we created when setting up a new forest in the domain, in our example called "marcosdomain.com/labuser"
</p>
<br />

<p>
<img src="https://i.imgur.com/y3HYotR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now after our domain controller is now online we will create a couple of organizational units inside of active directory, you can find those new folders at the top in this image being titled _ADMIN & _EMPLEYEES.
</p>
<br />

<p>
<img src="https://i.imgur.com/1Umkdmk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
As is it bad practice to use generic users to perfrom administrative task in the real world, we will now promote a user to admin and in our scenerio the new admin will be called "Jane admin" the screenhot above showcases the creation of such.
<br />

<p>
<img src="https://i.imgur.com/RVDbFNn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that we promoted "Jane to admin we will now logg off and log back in using janes admin credentials.
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






