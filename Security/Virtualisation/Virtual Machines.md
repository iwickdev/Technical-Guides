10.3.23 SkySRN

# What are Virtual Machines?

A VM is a virtualised instance of a computer that can perform almost all the same functions as a computer, including running applications and operating systems.

## What can they be used for? 

VMs can be used as an isolated environment with full functionality for testing and development, with no impact on the infrastructure that surrounds them.

They can also play a big role in disaster recovery on enterprise levels. System replication in cloud environments using virtual machines (VMs) can add an extra layer of security and assurance. Continuous updating is also possible in cloud systems.

## Setting up a Virtual Machine 

#### The Hypervisor 

- Choosing a Hypervisor 

You can choose from a wide variety of hypervisors on the market. The most well-known ones include VMware, VirtualBox, and HyperV. Since VirtualBox is the best available free alternative, we will be using it as our example throughout this guide.

- Installing the Hypervisor 

To finish the installation, download the VirtualBox [setup](https://www.virtualbox.org/wiki/Downloads) and follow the on-screen instructions.

#### The Operating System

Download the disc image (ISO file) of the operating system you want to use in your virtual machine. In this walkthrough, we'll be employing Windows 11/10.

You can get the ISO of Windows 10 [here](https://www.microsoft.com/en-in/software-download/windows10ISO), and Windows 11 [here](https://www.microsoft.com/software-download/windows11). 

#### Configuring the Virtual Machine 

##### Creating a Base for the Virtual Machine

- Once the VirtualBox GUI is open, click on **New** 
- Name the Virtual Machine 
- Choose the destination of the Virtual Machine
> Select a location where you have ample amount of storage
- Choose the ISO image of your operating system which you had installed 
- Check the box where it says **Skip Unattended Installation**
- Click **Next** and allot your Virtual Machine memory (RAM) and processors
> Keep a minimum of 2GB (2048MB) of RAM and 4 processors for considerable performance
- Click **Next** and create a virtual hard disk
> 80GB of storage is preferrable 
- Click **Next** and now you'll get a summary of the specifications of your virtual machine. Once reviewed and cross-checked click **Finish**

##### Securing the Virtual Machine

- Now you will be able to see your virtual machine in the left panel
- Right click on your Virtual Machine and click **Settings**
- Go to `General > Advanced` and make the following changes:

> Shared Clipboard - Bidirectional 

> Drag'n'Drop - Disabled

- Go to `Network > Enable Network Adapter (Check the box) > Attached to NAT`
  
  Or you could even just disable Network for your VM if you don't need it. This even makes it more secure, but again, keep it enabled if you want to access the internet
  
- If you want to have shared folders:

> `Shared folders > Add Shared Folder (Insert Key) > Select Folder Path > Name the Folder > Enable Read-only > Enable Auto-mount > Click OK`

##### The Guest OS

- Install your Operating system just like you would in a normal machine
- Keep your Guest OS (Windows in this case) updated always, so that it reduces the chances of anything malicious escaping the virtual machine
- Take a snapshot of the virtual machine so that you can revert back to a clean state if you break something.
  How to take snapshots:
> `If your VM is running > Click on Machine > Select Take Snapshots from the pull down menu`

> ` If the VM is turned off > Click on the Lists icon next to the machine name > Select Snapshots > Click on Take`


##### The Host OS

- Make sure your host operating system is always updated
- Keep an antivirus running

##### Hardening Windows Security Components in the Host OS

> Open the Windows Search Box > Type in Windows Security and open it > Virus and Threat Protection

When you've located to this location, follow along these steps: 

- You may turn on Memory Integrity, which isolates computer processes from your operating system and device to further defend against malware and other attacks by preventing harmful code from accessing high-security processes in the case of an attack.
- Enable TPM under Security Processor Details

  Your PC's security is increased using a TPM (Trusted Platform Module). It's used by programmes like Windows Hello and BitLocker drive encryption to safely generate and store cryptographic keys as well as to verify that the firmware and operating system on your device are what they should be and haven't been tampered with.
- Enable Secure Boot 

  When you turn on your device, secure boot blocks rootkits, a complex and deadly kind of malware, from loading. Because rootkits start before the operating system and use the same permissions, they can totally conceal themselves. Rootkits frequently come with a full arsenal of malicious software that can transfer private files, bypass local logins, record passwords and keystrokes, and capture cryptographic data.
  
  - You could also harden your Host OS with [DefenderUI](https://www.defenderui.com/) (optional)
  
After you've followed the above steps, you're free to use the Virtual Machine as you desire. 

**Note**: Please be highly cautious while running malware on your virtual machine and make use of common sense while doing so. If you're still unsure of your decision, please refrain and use cloud based virtual machines. There are plenty of such services online, some of them are listed below

- [Tria.ge](https://tria.ge/)
- [ANY.RUN](https://app.any.run/)
- [Cuckoo Sandbox](https://cuckoo.cert.ee/)
- [Joe Sandbox](https://www.joesandbox.com/#windows)
- [Linode](https://www.linode.com/)

  




