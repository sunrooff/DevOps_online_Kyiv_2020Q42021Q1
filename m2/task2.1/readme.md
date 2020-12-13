# Module 2 Virtualization and Cloud Basic.
## TASK 2.1
### PART 1. HYPERVISORS

1. **What are the most popular hypervisors for infrastructure virtualization?**
    - _the most popular are Xen (AWS), Oracle VM, vSphere (VMware), Hyper-V (Microsoft) and KVM (Linux, x86 platform)_</br></br>
2. **Briefly describe the main differences of the most popular hypervisors.**
    - _there are 2 types of hypervisors:_
      + _Type 1: they work and are installed right on the host's hardware in order to monitor and control guest machines_
         - _Xen (AWS); Oracle VM Server для SPARC_
         - _Oracle VM Server для x86_
         - _Hyper-V     (Microsoft)_
         - _VMware’s ESX/ESXi_
      + _Type 2: run on a regular OS just like other applications on the system. In this case, the guest OS operates as a process on the host,
      while the hypervisors separate the guest OS from the virtual machine operating system_


### PART 2. WORK WITH VIRTUALBOX
#### 1. First run VirtualBox and Virtual Machine (VM).

1.1 - 1.2) I briefly checked the VirtualBox manual; downloaded VirtualBox for Windows and downloaded latest Ubuntu desctop</br></br>
![1](./screenshots/1.2.png)</br>

1.3) Then I installed VirtualBox and Ubuntu 20.04.1 (with the proper name-title as per the guideline)</br></br>
![1](./screenshots/1.3.1.png)</br></br>
![1](./screenshots/1.3.png)</br>

1.4) Tried some possibilities of VM (start, stop, reboot, save state, host key).</br>
1.5) After that I've created a clone for the main VM.</br></br>
![1](./screenshots/1.5.png)</br>

1.6) Also I've created a group of two VMs</br></br>
![1](./screenshots/1.6.png)</br>

1.7) I tried to make a branched tree but it stood in one line (queue)</br></br>
![1](./screenshots/1.7.png)</br>

1.8) Exported and saved ova file of main VM to the local directory.</br>
After that ova file imported.</br></br>
![1](./screenshots/1.8.png)</br></br>
![1](./screenshots/1.8.1.png)</br></br>
![1](./screenshots/1.8.2.png)</br></br>
After the import :</br>
![1](./screenshots/1.8.3.png)</br></br>


#### 2. Configuration of virtual machines
2.1 - 2.2) I explored VM general configuration and managed to configure successfully USB between host and VM1.</br>

- during configuring of USB - additional plugin should be downloaded/installed into VirtulBox from the main website</br>

![1](./screenshots/2.2.png)</br></br>
![1](./screenshots/2.2.1.png)</br></br>


2.3) Successful configuration of shared folder between host and VM.</br></br>
![1](./screenshots/2.3.png)</br></br>
![1](./screenshots/2.3.1.png)</br></br>
![1](./screenshots/2.3.2.png)</br></br>
![1](./screenshots/2.3.3.png)</br></br>


2.4) I tested different network modes for VM1, VM2.</br>

![1](./screenshots/2.4.png)</br></br>
Ping each other VM1 and VM2 within "Local Bridge" connection type :</br>
![1](./screenshots/2.4.1.png)</br></br>
Also created a simple table with ping connection review :</br>
![1](./screenshots/2.4.2.png)</br>


#### 3. Work with CLI through VBoxManage.</br>
3.1 - 3.2) I generally explored CLI with VBoxManage (TBD)</br>
![1](./screenshots/2.5.1.png)</br></br>
Currently running VM :</br>
![1](./screenshots/2.5.2.png)</br>


### PART 3. WORK WITH VAGRANT

1-2) As per the instructions I've downloaded and installed Vagrant. Also I run PowerShell and checked Vagrant's version.</br>
![1](./screenshots/3.1.png)</br></br>

3-4) Initialization of the environment and it's launch</br>
![1](./screenshots/3.4.png)</br></br>
![1](./screenshots/3.4.1.png)</br>

5) ssh connection via Putty :  </br>
![1](./screenshots/3.5.1.png)</br></br>
ssh connection via MobaXterm :</br>
![1](./screenshots/3.5.png)</br></br>

6) Record of the time and date : </br>
![1](./screenshots/3.6.png)</br></br>

7) VM is stopped and deleted : </br>
![1](./screenshots/3.7.png)</br></br>

8) Vagrant box is created : </br>
![1](./screenshots/3.8.png)</br></br>

9) *(optional)* Create a test environment from a few servers. Servers' parameters
are chosen independently by the student.
</br> **TBD**


**PS.**
This time I used Atom (as an edit tool) to create readme.md file.
