<h1>Setting Up a HoneyPot in Microsoft Azure</h1>

![HPot](https://github.com/MMease/HoneyPot/assets/42321472/ff4121c2-1f9b-49c3-8774-c4504d0bf9ad)

<h2>Step 1: Create a Virtual Machine</h2>
In the Microsoft Azure cloud platform, the first step to set up your HoneyPot is to create a new Virtual Machine (VM) that will serve as the host for the honeypot environment. When creating the VM, it is essential to provide a meaningful and identifiable name, such as "Honeypot-VM-1," to distinguish it from other resources in your Azure environment.
Choose "Create a resource" from the Azure portal.
Search for "Virtual Machine" and select "Create" to begin VM creation.
Enter a unique name for the VM and select "Debian 11 "Bullseye" - ×64 Gen2" as the operating system image.
Choose an appropriate VM size based on the required CPU, memory, and storage resources for your honeypot.

![VM1](https://github.com/MMease/HoneyPot/assets/42321472/f6c489e2-386c-45f3-8f87-6745e70134c3)
![VM2](https://github.com/MMease/HoneyPot/assets/42321472/37af7903-67d8-4fa7-8b82-cd5671c00609)
![VM3 (Disk Creation   Setup)](https://github.com/MMease/HoneyPot/assets/42321472/4fd6e55a-4ee8-48ab-950f-340c9387e4a1)

<h3>Step 2: Installation & Configuration</h3>
Once your VM is ready, select it from the Azure portal, and go to the "Overview" section.
Navigate to the "Networking" section, and add an inbound Security Group to allow all traffic into the HoneyPot.

![Honeypot (Netwokring Traffic)](https://github.com/MMease/HoneyPot/assets/42321472/a4a62af3-bbf1-487e-b243-7138c30d2f8b)

Download PuTTY from (https://www.putty.org) to connect to your VM.
Use PuTTY to log in to your VM using the provided credentials and generate a private key using ("imported-openssh-key").

![Putty 1](https://github.com/MMease/HoneyPot/assets/42321472/9dec430e-09f6-4e7c-a7a1-7fece4654713)

1. Update the system and clone the T-Pot HoneyPot repository:

- sudo apt update
- sudo apt upgrade -y
- sudo apt install git
- sudo git clone https://github.com/telekom-security/tpotce

![Putty 2 (Post Configuration)](https://github.com/MMease/HoneyPot/assets/42321472/ab677192-8ab4-4e0f-b1b3-8317f3bf633a)

2. Navigate to the T-Pot installation directory and run the installation script:
- cd tpotce/iso/installer/
- sudo ./install.sh --type=user

![Putty 4 (Successful Tpot Installation)](https://github.com/MMease/HoneyPot/assets/42321472/e4851460-1153-45e9-8c56-27a27cbf56e6)

<h3>Step 3: T-Pot HoneyPot Interface</h3>
After a successful installation, you can access the T-Pot HoneyPot interface. The interface provides various options to view and analyze potential attacks.

![Tpot interface](https://github.com/MMease/HoneyPot/assets/42321472/02c0b641-f966-4f97-a1f5-b409285e3137)

Additionally, you can view real-time attack information on the live map:

![Tpot elastic live map attack](https://github.com/MMease/HoneyPot/assets/42321472/19f4aa09-90f0-4b2a-a649-84a22fd3344c)

Remember, running a HoneyPot carries inherent risks, so it's crucial to operate it within a controlled and secure environment. Only experienced cybersecurity professionals should undertake such initiatives.

