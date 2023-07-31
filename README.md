<h1>HoneyPot In Azure</h1>

![HPot](https://github.com/MMease/HoneyPot/assets/42321472/ff4121c2-1f9b-49c3-8774-c4504d0bf9ad)


<h2>Create a Virtual Machine</h2>
In the Microsoft Azure cloud platform, to set up your honeypot, the first step is to create a new Virtual Machine (VM) that will serve as the host for the honeypot environment. When creating the VM, it is essential to provide a meaningful and identifiable name, which could be something like "Honeypot-VM-1" or any other name that helps you distinguish it from other resources in your Azure environment.

After naming the VM, when selecting the operating system image for the machine, opt for "Debian 11 "Bullseye" - ×64 Gen2". Debian 11 "Bullseye" is a popular Linux distribution known for its stability and wide community support, making it an excellent choice for running a honeypot. The next crucial aspect to consider is choosing the appropriate size for the virtual machine. The VM size determines the amount of CPU, memory, and storage resources allocated to the honeypot.

![VM1](https://github.com/MMease/HoneyPot/assets/42321472/f6c489e2-386c-45f3-8f87-6745e70134c3)
![VM2](https://github.com/MMease/HoneyPot/assets/42321472/37af7903-67d8-4fa7-8b82-cd5671c00609)
![VM3 (Disk Creation   Setup)](https://github.com/MMease/HoneyPot/assets/42321472/4fd6e55a-4ee8-48ab-950f-340c9387e4a1)


<h3>Installaton & Configuration </h3>

First you want to select the VM you just created. When it opens you will see an <b>"Overview"</b> section. Next, you will select the <b>"Networking"</b> section where you will add an inbound Security group. This will allow all traffic to come into the HoneyPot.

![Honeypot (Netwokring Traffic)](https://github.com/MMease/HoneyPot/assets/42321472/a4a62af3-bbf1-487e-b243-7138c30d2f8b)

- We are going to download putty using this link (https://www.putty.org).
- Enter your VMs IP Address into putty
- Login using the credential from the VM.
- Generate a private key using <b>"imported-openssh-key"</b>.
  
![Putty 1](https://github.com/MMease/HoneyPot/assets/42321472/9dec430e-09f6-4e7c-a7a1-7fece4654713)

Use the following commands to <b> update and clone a github repository </b> which we will be using to access the honeypot:
- sudo apt update
- sudo apt upgrade -y
- sudo apt install git
- sudo git clone https://github.com/telekom-security/tpotce
- sudo cd tpotce/iso/installer/
- sudo ./install.sh --type=user

![Putty 2 (Post Configuration)](https://github.com/MMease/HoneyPot/assets/42321472/ab677192-8ab4-4e0f-b1b3-8317f3bf633a)
![Putty 3 (Updating)](https://github.com/MMease/HoneyPot/assets/42321472/96f37f6a-297c-4ef6-bae1-e21c174b718b)

This is how it looks after a successful installaion.

![Putty 4 (Successful Tpot Installation)](https://github.com/MMease/HoneyPot/assets/42321472/e4851460-1153-45e9-8c56-27a27cbf56e6)


This shows the user interface for the HoneyPot. It has several different options that gives different interfaces and Information.

![Tpot interface](https://github.com/MMease/HoneyPot/assets/42321472/02c0b641-f966-4f97-a1f5-b409285e3137)

This shows us a representation of different attacks on a live map.

![Tpot elastic live map attack](https://github.com/MMease/HoneyPot/assets/42321472/19f4aa09-90f0-4b2a-a649-84a22fd3344c)



