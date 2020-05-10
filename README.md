# WINFINGER

This repository contains various windows fingerprint files generated against base ISO images.

**Coverage**

The following operating system versions were hashed:

| Windows Version | x86 | x64 | Base install.wim hash | Base boot.wim hash | 
| ------------- | ------------- | ------------- | ------------- |
| Windows Vista Home Basic | Yes | Yes | Yes | Yes | 
| Windows Vista Home Premium | Yes | Yes | Yes | Yes | 
| Windows Vista Business | Yes | Yes | Yes |  Yes | 
| Windows Vista Ultimate | Yes | Yes | Yes |  Yes | 
| Windows Vista Starter | Yes | No | Yes | Yes | 
| Windows Vista Enterprise | Yes | Yes | Yes | Yes | 


** Methodology ** 

* For each ISO:
 * Extract boot.wim and install.wim
 * Hash ISO file to generate SHA1
 * Unpack boot.wim and install.wim to folder named after SHA1 of the ISO
 * Use sigcheck64.exe from [Sysinternals](https://docs.microsoft.com/en-us/sysinternals/) to create signature files for extracted archives
 * Create 7zip of corresponding directory

