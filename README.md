# Deploying Active Directory (on premises) and Creating Users

<p align="center">
<p>
<img src="https://i.imgur.com/2oMXnpT.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
</p>


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Powershell
- Active directory services 


<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Windows Server 2022


<p>
<img src="https://i.imgur.com/JfZE9ed.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this lab, the objective is to create two virtual machines (VMs) within the same virtual network (VNET). The first VM will serve as the Domain Controller, providing Active Directory services. To ensure consistent communication, a static IP will be assigned to the Domain Controller. The second VM will be the Client machine, which will be joined to the domain established by the Domain Controller.
</p>
<br />



<p>
<img src="https://i.imgur.com/tHTcq6M.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To ensure connectivity between DC-1 and Client-1, it is necessary to assign a static Private IP Address to DC-1. Initially, the ping between DC-1 and Client-1 may not work properly. To address this, you need to enable ICMPv4 on the firewall of DC-1. After enabling ICMPv4, you will be able to successfully ping DC-1 from Client-1, establishing the desired connectivity.
</p>
<br />

<p>
<img src="https://i.imgur.com/xpd1EoX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

The provided screenshot confirms that after enabling ICMPv4 on the firewall, we have established successful connectivity.
</p>
<br />

<p>
<img src="https://i.imgur.com/jEHDGyt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The image above showcases the process of logging into our DC-1 virtual machine (VM) and initiating the installation of Active Directory Domain Services. Subsequently, we proceed to promote it as our domain controller.
</p>
<br />

<p>
<img src="https://i.imgur.com/GrSr2mn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Soon after restarting DC-1, we will now log back into the converted domain controller using our domain credentials that were created during the setup of a new forest in the domain. In our example, the domain credentials are "marcosdomain.com/labuser."
</p>
<br />

<p>
<img src="https://i.imgur.com/y3HYotR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After bringing our domain controller online, we will proceed to create a couple of organizational units within Active Directory. You can locate these new folders, labeled as "_ADMIN" and "_EMPLOYEES," at the top of the image provided.
</p>
<br />

<p>
<img src="https://i.imgur.com/1Umkdmk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
It is considered a best practice to avoid using generic user accounts for administrative tasks in real-world scenarios. In line with this principle, we will now promote a specific user to the admin role. In our scenario, the newly designated admin will be named "Jane admin." The screenshot above illustrates the creation of this user with administrative privileges.
<br />

<p>
<img src="https://i.imgur.com/RVDbFNn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that we have promoted "Jane" to an admin role, we will proceed to log off and then log back in using Jane's admin credentials.
</p>
<br />

<p>
<img src="https://i.imgur.com/zX4HUmi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To demonstrate a successful login as Jane_admin, you can open the command prompt and enter the command "whoami." This will display the logged-in user as Jane_admin.
</p>
<br />

<p>
<img src="https://i.imgur.com/Xlr0r04.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Going forward, please use the administrator account 'Jane_admin.' Our next step is to join Client-1 to the domain (mydomain.com) using the Azure portal. To accomplish this, update Client-1's DNS settings with the private IP address of the DC (Domain Controller). Once the DNS settings are updated, restart Client-1 from within the Azure portal. The image below serves as verification that Client-1 is now utilizing DC-1 DNS.
</p>
<br />

<p>
<img src="https://i.imgur.com/Ks2Mhlw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that Client-1 is part of the domain, we will proceed to configure remote desktop access for non-administrative users. To do this, log in to Client-1 as an administrator and open the system properties. From there, navigate to the 'Remote Desktop' section and grant 'domain users' access to remote desktop. Once these steps are completed, you should be able to log into Client-1 as a normal user
</p>
<br />

<p>
<img src="https://i.imgur.com/NDoQwU3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To confirm whether normal users can RDP into Client-1, we will employ a PowerShell script to generate a large number of users within the domain. Once the users have been created, we will proceed to select one and initiate an RDP session to connect to Client-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/s0PaZAy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />


<p>
<img src="https://i.imgur.com/4dCZ48E.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
As you can see, we were able to select a random user from our user generation script, and they were able to log in using their own credentials
that concludes this lengthy lab. Thank you if you made it this far.

</p>
<br />







