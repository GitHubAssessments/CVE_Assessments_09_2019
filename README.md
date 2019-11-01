# CVE_Assessments_09_2019

This is the Enpass-setup.exe

Source: 
https://www.enpass.io/

https://dl.enpass.io/stable/windows/setup/6.2.0.539/Enpass-setup.exe

MD5 4686ebde7c4c93c5538b85949477a624

SHA-1 4c747d3b84ebe7deedf03db32f1d0daa33d1c175

SHA-256 4ad268b913f589513d167aa2591ed806cadcb0ec5e1c3154378ca334b5adc87b

https://www.virustotal.com/gui/file/4ad268b913f589513d167aa2591ed806cadcb0ec5e1c3154378ca334b5adc87b/behavior/VirusTotal%20Jujubox

And the software is dropping the following files:

1) C:\Windows\Temp{7C04766E-9547-4E72-BA11-3C0EB2560AE7}\.cr\Enpass-setup.exe
sha256 ce1e66c55264e06f72a64ad0a9a15104bf9cbc0602222107c492008b02bbf85e

Which creates the following change in the Windows Registry:

\Registry\Machine\Software\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\996E.exe

and Create a Mutex

CTF.LBES.MutexDefaultS-1-5-21-1482476501-1645522239-1417001333-500

https://www.virustotal.com/gui/file/ce1e66c55264e06f72a64ad0a9a15104bf9cbc0602222107c492008b02bbf85e/behavior/Tencent%20HABO

That are very similar to a known malware:

https://sensorstechforum.com/waifu-files-virus-dharma-ransomware-remove-restore-data/


2) Also the installer refers to a WiX toolset:
C:\Windows\Temp{26B60979-3787-4506-BC8B-70B6D7E42B09}\.ba\wixstdba.dll
sha256 7b9f919a3d1974fd8fa35ad189edc8bf287f476bd377e713e616b26864a4b0d3

However the WiX Toolset was found recently vulnerable:

https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-16511
