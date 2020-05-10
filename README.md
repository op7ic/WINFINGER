# WINFINGER

This repository contains various windows fingerprint files generated against base ISO images.

**Coverage**

The following operating system versions were hashed:

| Windows Version | x86 | x64 | Base install.wim hash | Base boot.wim hash | 
| ------------- | ------------- | ------------- | ------------- |
| Windows Vista Home Basic | Yes | Yes | Yes | 
| Windows Vista Home Premium | Yes | Yes | Yes | 
| Windows Vista Business | Yes | Yes | Yes |  
| Windows Vista Ultimate | Yes | Yes | Yes |  
| Windows Vista Home Basic N | Yes | Yes | Yes | 
| Windows Vista Business N | Yes | Yes | Yes |  
| Windows Vista Starter | Yes | No | Yes | 
| Windows Vista Enterprise | Yes | Yes | Yes | 
| Windows 7 Starter | No | No | No | 
| Windows 7 Home Basic | No | No | No | 
| Windows 7 Home Premium | No | No | No | 
| Windows 7 Professional | No | No | No | 
| Windows 7 Enterprise | No | No | No | 
| Windows 7 Ultimate | No | No | No | 
| Windows 8 | No | No | No | 
| Windows 8 Pro | No | No | No | 
| Windows 8 Enterprise | No | No | No | 
| Windows 8.1 | No | No | No | 
| Windows 8.1 Pro | No | No | No | 
| Windows 8.1 Enterprise | No | No | No | 
| Windows 10 Home  | No | No | No | 
| Windows 10 Pro | No | No | No | 
| Windows 10 Enterprise | No | No | No | 
| Windows 10 Enterprise LTSB | No | No | No | 
| Windows 10 Education | No | No | No | 
| Windows 10 Pro Education | No | No | No | 
| Windows 10 IoT Core | No | No | No | 


** Methodology ** 

* For each ISO:
 * Extract boot.wim and install.wim
 * Hash ISO file to generate SHA1
 * Unpack boot.wim and install.wim to folder named after SHA1 of the ISO
 * Use sigcheck64.exe from [Sysinternals](https://docs.microsoft.com/en-us/sysinternals/) to create signature files for extracted archives

