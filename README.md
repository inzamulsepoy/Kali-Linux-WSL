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
Check on - Windows Subsystem for Linux, Virtual Machine Platform, Windows Sandbox  <br>

RESTART <br>

Run Windows PowerShell as administrator <br>
run this command<br>
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux 
```

RESTART <br>

run this command<br>
```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
run this command<br>
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
RESTART <br>

Download Linux Kernel: https://aka.ms/wsl2kernel <br>

Download the latest package <br>

and install it <br>

<h3>SET DEFAULT TO WSL 2</h3>

Open Windows PowerShell as Administrator<br>

run the command <br>
```
wsl --set-default-version 2
```

go to the microsoft store <br>
and download kali linux App <br>

Open it after downloading & installing <br>

create a username and password <br>

run - 
```
cat /etc/os-release
```
<h3>INSTALL GUI</h3>
  
run the commands<br>
```  
sudo apt update && sudo apt upgrade -y
```
```
sudo apt install kali-desktop-xfce -y
```
CHECK VERSION <br>
open Windows PowerShell and run the command <br>
```
wsl --list --verbose
```
<h3>XRDP - Remote Desktop Protocol</h3>

run the following commands <br>
```
sudo apt install xrdp -y
```
```
sudo service xrdp start
```
run - 
```
ip add
```
and copy the ipaddress after inet <br>

search for remote desktop connection in windows <br>
paste the ip address <br>

login with the createad username and password
