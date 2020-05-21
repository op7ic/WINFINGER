# WINFINGER

This repository contains windows OS fingerprint files generated against both 'install' and 'boot' WIM archives.

**Coverage**

The following families of operating system versions were hashed:

| Windows Version | x86 | x64 | Base install.wim hash | Base boot.wim hash | 
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Windows Vista | Yes | Yes | Yes | Yes | Yes | 
| Windows Vista Ultimate | Yes | Yes | Yes | Yes | 
| Windows Vista Enterprise | Yes | Yes | Yes | Yes | 
| Windows 7 Debug Checked | Yes | Yes | Yes | Yes | 
| Windows 7 Embedded POSReady | Yes | Yes | Yes | Yes | 
| Windows 7 Embedded Standard | Yes | Yes | Yes | Yes | 
| Windows 7 Enterprise | Yes | Yes | Yes | Yes | 
| Windows 7 Home Basic | Yes | No | Yes | Yes | 
| Windows 7 Home Professional | Yes | No | Yes | Yes | 
| Windows 7 Professional | Yes | Yes | Yes | Yes | 
| Windows 7 Starter | Yes | No | Yes | Yes | 
| Windows 7 Ultimate | Yes | Yes | Yes | Yes | 
| Windows 8 | Yes | Yes | Yes | Yes | 
| Windows 8 Embedded Industry Pro | Yes | Yes | Yes | Yes | 
| Windows 8 Enterprise | Yes | Yes | Yes | Yes | 
| Windows 8 Pro | Yes | Yes | Yes | Yes | 
| Windows 8.1 Debug Checked | Yes | Yes | Yes | Yes | 
| Windows 8.1 Embedded | Yes | Yes | Yes | Yes | 
| Windows 8.1 Enterprise | Yes | Yes | Yes | Yes | 
| Windows 8.1 Pro | Yes | Yes | Yes | Yes | 
| Windows 8.1 | Yes | Yes | Yes | Yes | 
| Windows 10 Business Editions | Yes | Yes | Yes | Yes | 
| Windows 10 Consumer Editions | Yes | No | Yes | Yes | 
| Windows 10 Education | Yes | Yes | Yes | Yes | 
| Windows 10 Enterprise | Yes | Yes | Yes | Yes | 
| Windows 10 IOT | Yes | Yes | Yes | Yes | 
| Windows 10 | Yes | Yes | Yes | Yes | 
| Windows Server 2008 | Yes | Yes | Yes | Yes | 
| Windows Server 2008 Web Server | Yes | Yes | Yes | Yes | 
| Windows Server 2008R2 | No | Yes | Yes | Yes | 
| Windows Server 2012 | No | Yes | Yes | Yes | 
| Windows Server 2012 Debug Checked | No | Yes | Yes | Yes | 
| Windows Server 2012 Multipoint Premium | No | Yes | Yes | Yes | 
| Windows Server 2012 Multipoint Standard | No | Yes | Yes | Yes | 
| Windows Server 2012 Storage Server Foundation | No | Yes | Yes | Yes | 
| Windows Server 2012R2 | No | Yes | Yes | Yes | 
| Windows Server 2012R2 Debug Checked | No | Yes | Yes | Yes | 
| Windows Server 2012R2 Essentials | No | Yes | Yes | Yes | 
| Windows Server 2016 Essentials | No | Yes | Yes | Yes | 
| Windows Server 2016 | No | Yes | Yes | Yes | 
| Windows Server 2016 Storage Server | No | Yes | Yes | Yes | 
| Windows Server 2019 Essentials | No | Yes | Yes | Yes | 
| Windows Server 2019 | No | Yes | Yes | Yes | 
| Windows Server 1709 | No | Yes | Yes | Yes | 
| Windows Server 1803 | No | Yes | Yes | Yes | 
| Windows Server 1809 | No | Yes | Yes | Yes | 
| Windows Server 1903 | No | Yes | Yes | Yes | 
| Windows Server 1909 | No | Yes | Yes | Yes | 


**Methodology** 

* For each ISO:
 * Extract boot.wim and install.wim
 * Hash ISO file to generate SHA1
 * Unpack boot.wim and install.wim to folder named after SHA1 of the ISO
 * Use sigcheck64.exe from [Sysinternals](https://docs.microsoft.com/en-us/sysinternals/) to create signature files for binary files from extracted archives
 * Create 7zip of corresponding directory

**Getting Hashes out**

- Convert all files to unix format for easy grepping using ```$ dos2unix.exe -f */*.csv``` command. 
- grep/awk hash type you need or use csvtool

**Removing Headers**
If headers need to be removed and CVS adjusted for easy parsing, run the following ``sed`` commands:
```
sed -i -e '/Sigcheck v2.73 - File version and signature viewer/d' */*
sed -i -e '/Copyright (C) 2004-2019 Mark Russinovich/d' */*
sed -i -e '/Sysinternals - www.sysinternals.com/d' */*
sed -i -e '1{/^$/d}' */*
sed -i -e '1{/^$/d}' */*
```

** TODO **

[ ] Hash Windows Updates
