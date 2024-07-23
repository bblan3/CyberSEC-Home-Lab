# Home-Lab
#### This lab was created to simulate a comprehensive network environment, compiled of Windows Server 2022, a Windows user, Kali Linux and Metasploitable. Goal of remediating identified vulnerabilities in order to strengthen security.

### Setup 

Router -> Physical Host Running Windows 10 -> 4 VMs running through Oracle Virtual Box.


Virtual Machines 
- 
#### Windows Server 2022
- A virtualized Windows Server can host multiple users, utilizing Active Directory for scalability and ability to manage user accounts centrally. 

#### Windows 10 Enterprise
- Represents a typical user machine within the domain.

#### Kali Linux
- Serves as the attacker machine for penetration testing with tons of cybersecurity-related tools already installed.

#### Metasploitable
- Loaded with known vulnerabilities used for testing tools and techniques.

![VMs](https://github.com/user-attachments/assets/255a6a99-4360-4222-9c24-d2bd0fea2025)


 ### Configuring ACTIVE DIRECTORY -  Windows Server 2022

 ![AD](https://github.com/user-attachments/assets/44f40d25-af28-4957-8b44-b9522a19432f)

This is the Server manager that appears when you log into Windows Server 2022.

![Adding Features](https://github.com/user-attachments/assets/c2be65aa-b340-4884-9c0f-2dd90c23375d)
Now I will add the features that we want, I'm adding an Active Directory domain and DNS.

Once I configured the domain controller, I added two accounts.
A user account, pictured here
![User SOC](https://github.com/user-attachments/assets/df909867-1e54-4694-8246-166123633002)

An admin account pictured here
![Admin SOC](https://github.com/user-attachments/assets/5cd2a3f2-3ce4-409a-8244-b72ae57a8ae2)

### Port Scan and Security
Now that we have set up roles, users and services, lets scan for open ports.
![port scan](https://github.com/user-attachments/assets/f299acc1-96fb-4721-9fd9-b28b96e6e4ca)

Now, the port scan returned 11 open ports but some of these need to remain open.
We now will need to determine which services our devices and applications require. Turn off any services that are not needed, this will automatically close associated ports.

Once we have decided which ports to close and which can remain open, we need to create a new rule according to our decision.

![Blocking ports](https://github.com/user-attachments/assets/bdbea81f-3452-41dc-a273-f11d176d8870)

Overview
-
### Server Setup
- Created SOC domain for simple user management
- Added DNS server

### Network Configuration
- VLAN setup to implement segmentation
- VMs network tab were set to bridged mode

### Security Measures
- Firewall rules for traffic filtering
- VLAN segregation for network isolation
- Specific role based access on individual machines for hardening

## Conclusion
This home lab is a way to practice cybersecurity skills and techniques to gain hands on experience and learning.
