# WINFINGER

This repository contains various windows fingerprint files generated against based image and base images updated by windows update (where possible). 

**Coverage**

The following operating system versions were hashed:

| Windows Version | x86 | x64 | Base OS Hashed? | Service Pack | 
| ------------- | ------------- | ------------- | ------------- | 
| Windows Vista Home Basic | Yes | Yes | Yes | N/A |
| Windows Vista Home Premium | Yes | Yes | Yes | N/A |
| Windows Vista Business | Yes | Yes | Yes | N/A | 
| Windows Vista Ultimate | Yes | Yes | Yes | N/A | 
| Windows Vista Home Basic N | Yes | Yes | Yes | N/A |
| Windows Vista Business N | Yes | Yes | Yes | N/A | 
| Windows Vista Starter | Yes | No | Yes | N/A |
| Windows Vista Enterprise | Yes | Yes | Yes | N/A |
| Windows XP Professional | No | Yes | No | SP1 | 
| Windows XP Professional | Yes | No | Yes | SP3 | 

TODO:

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
| Windows 10 Enterprise | No | No | No | N/A |
| Windows 10 Enterprise LTSB | No | No | No | N/A |
| Windows 10 Education | No | No | No | N/A |
| Windows 10 Pro Education | No | No | No | N/A |
| Windows 10 IoT Core | No | No | No | N/A |


** Methodology ** 

* Using Packer build each of the above versions as VirtualBox VM
* Mount created VMDK as partition using FTK Imager
* Use Sigcheck from Sysinternals to create hash of all the binaries in partition, output to CSV
* Install Sysmon
* Allow for full updates while sysmon logs all hashes up to latest patch/version
* Extract all hashes from Sysmon

** Naming Convention ** 

Each file is named using the same naming convention:

*(Windows Version)_(x64 or x86)_(Major Edition)_(Service Pack, if any)_(Minor Edition, if any)_(updated or base)*

For example, the following filename would correspond to Windows XP Professional 64 bit with Service Pack 2, base image: 

* WindowsXP_x64_professional_SP3_base.csv *

For example, the following filename would correspond to Windows XP Professional N 64 bit with Service Pack 2, base image: 

* WindowsXP_x64_professional_SP3_n_base.csv *

