# Kali-Linux-WSL installation guide
Complete Guide to install Kali Linux in windows-WSL

<h1>INSTALL WSL 2</h1>
<h2>Step 1</h2>

Check your windows version.
win + R <br>

```
winver
```
It should be above 19041 <br>

<h2>Step 2</h2>

Enable- WindowsOptionalFeature <br>
write in win + R<br>
```
optionalfeatures
```
Check on - Windows Subsystem for Linux, Virtual Machine Platform <br>

RESTART <br>

<h2>Step 3</h2>

Run Windows PowerShell as administrator <br>
run this command<br>
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux 
```

RESTART <br>

<h2>Step 4</h2>

run this command<br>
```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

run this command<br>
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
RESTART <br>

<h2>Step 5</h2>
Download Linux Kernel: https://aka.ms/wsl2kernel <br>

Download the latest package <br>

and install it <br>

<h2>Step 6</h2>

<h3>SET DEFAULT TO WSL 2</h3>

Open Windows PowerShell as Administrator<br>

run the command <br>
```
wsl --set-default-version 2
```
<h2>Step 7</h2>
go to the microsoft store <br>
and download kali linux App <br>

Open it after downloading & installing <br>

<h2>Step 8</h2>

create a username and password <br>

run - 
```
cat /etc/os-release
```
<h2>Step 9</h2>
<h3>INSTALL GUI</h3>
  
run the commands<br>
```  
sudo apt update && sudo apt upgrade -y
```
```
sudo apt install kali-desktop-xfce -y
```
<h2>Step 10</h2>
CHECK VERSION <br>
open Windows PowerShell and run the command <br>

```
wsl --list --verbose
```

<h2>Step 11</h2>
<h3>XRDP - Remote Desktop Protocol</h3>

run the following commands <br>
```
sudo apt install xrdp -y
```
```
sudo service xrdp start
```
<h2>Step 12</h2>

Run the command in kali linux terminal

```
ip add
```

Copy the ipaddress after inet <br>

<h2>Step 13</h2>
Search for remote desktop connection in windows <br>
Paste the ip address <br>

<h2>Step 14</h2>
Login with the created username and password
