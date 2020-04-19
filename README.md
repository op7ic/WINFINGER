# WINFINGER

This repository contains various windows fingerprint files generated against based image and base images updated by windows update. 

**Coverage**

The following operating system versions were hashed:

| Windows Version | x86 | x64 | Base + Update | Service Pack | 
| ------------- | ------------- | ------------- | ------------- | 
| Windows XP | No | No | No | SP1 | 
| Windows XP | No | No | No | SP2 | 
| Windows XP | No | No | No | SP3 | 
| Windows Vista Starter | No | No | No | N/A |
| Windows Vista Home Basic | No | No | No | N/A |
| Windows Vista Home Premium | No | No | No | N/A |
| Windows Vista Business | No | No | No | N/A |
| Windows Vista Enterprise | No | No | No | N/A | 
| Windows Vista Ultimate | No | No | No | N/A | 
| Windows 7 Starter | No | No | No | N/A |
| Windows 7 Home Basic | No | No | No | N/A |
| Windows 7 Home Premium | No | No | No | N/A |
| Windows 7 Professional | No | No | No | N/A |
| Windows 7 Enterprise | No | No | No | N/A |
| Windows 7 Ultimate | No | No | No | N/A |
| Windows 8 | No | No | No | N/A |
| Windows 8 Pro | No | No | No | N/A |
| Windows 8 Enterprise | No | No | No | N/A |
| Windows 8.1 | No | No | No | N/A |
| Windows 8.1 Pro | No | No | No | N/A |
| Windows 8.1 Enterprise | No | No | No | N/A |
| Windows 10 Home  | No | No | No | N/A |
| Windows 10 Pro | No | No | No | N/A |
| Windows 10 Mobile | No | No | No | N/A |
| Windows 10 Enterprise | No | No | No | N/A |
| Windows 10 Enterprise LTSB | No | No | No | N/A |
| Windows 10 Mobile Enterprise | No | No | No | N/A |
| Windows 10 Education | No | No | No | N/A |
| Windows 10 Pro Education | No | No | No | N/A |
| Windows 10 IoT Core | No | No | No | N/A |


** Methodology ** 

* Using Packer build each of the above versions as VirtualBox VM
* Hash the base image files in VMDK
* Install Sysmon
* Allow for full updates while sysmon logs all hashes
* Extract all hashes from Sysmon
