# Kali-Linux-WSL installation guide
Complete Guide to install Kali Linux in windows-WSL

<h2>INSTALL WSL 2</h2>

# Check your windows version.
win + R <br>
winver <br>
it should be above 19041 <br>

Enable- WindowsOptionalFeature <br>
write in win + R<br>
optionalfeatures<br>
Check on - Windows Subsystem for Linux, Virtual Machine Platform, Windows Sandbox  <br>

RESTART <br>

Run Windows PowerShell as administrator <br>
run this command<br>
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux  <br>

RESTART <br>

run this command<br>

dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart<br>

run this command<br>

dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart  <br>

RESTART <br>

Download Linux Kernel: https://aka.ms/wsl2kernel <br>

Download the latest package <br>

and install it <br>

<h3>SET DEFAULT TO WSL 2</h3>

Open Windows PowerShell as Administrator<br>

run the command <br>

wsl --set-default-version 2 <br>


go to the microsoft store <br>
and download kali linux App <br>

Open it after downloading & installing <br>

create a username and password <br>

run - cat /etc/os-release <br>

<h3>INSTALL GUI</h3>
  
run the commands<br>
  
sudo apt update && sudo apt upgrade -y <br>

sudo apt install kali-desktop-xfce -y <br>

CHECK VERSION <br>
open Windows PowerShell and run the command <br>
wsl --list --verbose <br>

<h3>XRDP - Remote Desktop Protocol</h3>

run the following commands <br>

sudo apt install xrdp -y <br>
sudo service xrdp start <br>

run - ip add <br>
and copy the ipaddress after inet <br>

search for remote desktop connection in windows <br>
paste the ip address <br>

login with the createad username and password
