# Setting Up a Home Lab

## Objective

The goal of this Home Lab Setup project is to practice installing Windows OS and Kali Linux through the use of Vmware. These two operating systems will then be used as a part of my home lab so that I can gain hands-on experience with various tools, software, and concepts. 

### Skills Learned

- VM installation and naviagtion
- Installation of the Windows OS through the use of an .iso file. 
- Installation of Kali Linux through the use of an .iso file.
- Uninstallment of a VM 

### Tools Used

-Vmware: the hypervisor for my virtual machine.

---
## Steps

## Hypervisor Installation and Navigation

VMware is a type 1 hypervisor, meaning that it utilizes the hardware of its host machine to function. This is a huge benefit because it allows for direct hardware access, no host OS dependency, and has an entreprise focus. I will use VMware to run many virtual machines, starting with a Windows 10 and Linux VM. 

1. I first navigated to VMware's website and downloaded **Vmware Workstation Pro for Windows**.
2. Then, to ensure that no files were corrupted during the download, I used the **Get-FileHash** command in Powershell and compared the SHA256 strings.
   
![HomeLabImg1](https://github.com/user-attachments/assets/b71b64d9-33db-485f-b648-ac284ebbbce3)
(Downloading Vmware Workstation Pro for Windows)

---
## Installation of the Windows OS through the use of an .iso file

1. First, I visited Microsoft's website to download the Windows 10 .iso.
2. After completing the download, I added the .iso to Vmware by clicking *File,* then *New Virtual Machine,* and then completing the setup wizard to install Windows. I allocated **4 GB of memory and 2 CPUs**.
3. Next, I selected **I do not have a product key** during the boot and then installed **Windows Pro**.
4. Then, I selected **Custom** and installed the OS to Drive 0, with 60 GB of space.
5. After that, I selected the **Offline account** option and set my username, password, and 3 security questions.
6. Finally, after skipping a few services, my Windows VM booted up and I logged in with the password I set during the previous step. 
   
![HomeLabImg2](https://github.com/user-attachments/assets/b13ef1ae-0363-472f-93cc-06e4344a4019)
(Windows VM boot)

(Windows VM all set-up)

---
## Installation of Kali Linux through the use of an .iso file

1. First, I navigated to **kali.org** and downloaded the **x86_64 Installer Image.**
2. After it installed, I added the .iso to Vmware by clicking *File* and then *New Virtual Machine.* Unlike during the Windows installation, I made sure to select **Linux** as the Guest Operating System and **Debian 11.x 64-bit** as the Version (Kali is a Debian-based distribution of Linux).
3. Next, I allocated **4 GB of memory and 2 CPUs** to the VM and booted it up.
   
    ![HomeLabImg3](https://github.com/user-attachments/assets/bec76f03-1018-4189-96ff-8dda0c86324b)
    (What I saw after installing the VM)

4. To continue, I selected **Graphical Install** and proceeded through the language and keyboard setup until I gave provided the machine's hostname.
5. After providing the host name, I provided a made-up domain name, my full name, a Username for my account, a password, and my timezone.
6. Then, I partitioned the disks using the **Guided - use entire disk** option and the **All files in one partition.**
7. Furthermore, I selected every software available to install with Kali (GNOME, Xfce, KDE Plasma, etc) and kept the display manager selected to **gdm3**.
8. A pop-up to install the GRUB boot loader came up as the installation neared the end, and I selected **yes** and **/dev/sda** as the device for the boot loader installation.
9. Finally, after entering my login credentials, I gained access to my freshly installed Kali Linux VM.
    ![HomeLabImg4](https://github.com/user-attachments/assets/b7475c4e-c8a4-470b-93a8-773371f3ac79)
    (Freshly installed Kali Linux VM)

---
## Uninstallment of a VM 

|-| Remember how in step 2 I said that I made sure to select **Debian 11.x 64-bit** as the Version? Well, I learned what happens when you select an incorrect, incompatible version after I received an error while the system attempted to install the base package. Realizing that I selected the wrong version, I decided to uninstall the VM and all of it's associated files. 

1. To accomplish this, I first powered off the Linux VM.
2. Then, I right-clicked the VM and selected **Manage** and then **Delete from Disk.**
3. To confirm the Vms deletion, I both checked the VM Library and my ~\Documents\Virtual-Machines folder (where all of my Vms are saved) for the VM.

|-| After confirming the VMs deletion, I took a snapshot so that I can revert back to these fresh VMs whenever needed. 

## Conclusion

|-| In this project, I learned how to install and navigate a type-1 hypervisor (VMware) as well as install Windows and Linux to a VM. I also learned how to properly uninstall a VM. Windows and Linux are widely used in the IT and cybersecurity world to defend systems, networks, and organizations. As such, knowledge of how to install and use those two operating systems is very important, and this project has provided me with those skills. I also learned how to troubleshoot installation errors while trying to install Linux, as well as ways to correct them. 






