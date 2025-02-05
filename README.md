# Kali-Linux-WSL
Kali Linux in WSL

<h2>1. INSTALL WSL 2</h2>

Check your windows version.
win + R
cmd
winver
it should be above 19041

RUN POWERSHELL as administrator

Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux <br>

RESTART <br>
👉 dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

👉 dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

RESTART <br>

Download Linux Kernel: https://aka.ms/wsl2kernel

SET DEFAULT TO WSL 2
👉 wsl --set-default-version 2

CHECK VERSION 
👉 wsl --list --verbose

2. INSTALL GUI

👉 sudo apt update && sudo apt upgrade -y

👉 sudo apt install kali-desktop-xfce -y

XRDP

👉 sudo apt install xrdp -y

👉 sudo service xrdp start
