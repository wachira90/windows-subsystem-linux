# ENABLE Windows-Subsystem-Linux

Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

# REBOOT

# Manually download Windows Subsystem for Linux distro packages

https://docs.microsoft.com/en-us/windows/wsl/install-manual

# Download using PowerShell

Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing

# Download using curl

curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604

# Installing your distro

Add-AppxPackage .\app_name.appx


https://wslstorestorage.blob.core.windows.net/wslblob/Ubuntu_1804.2019.522.0_x64.appx

# RENAME AND EXTRACT

Rename-Item .\Ubuntu_1804.2019.522.0_x64.appx .\Ubuntu_1804.2019.522.0_x64.zip

Expand-Archive .\Ubuntu_1804.2019.522.0_x64.zip .\Ubuntu_1804.2019.522.0_x64


## Add your distro path to the Windows environment PATH (C:\Users\Administrator\Ubuntu in this example), using PowerShell:

$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")


Lunch => ubuntu.exe

# FILE LOCATION

C:\Users\NAME\AppData\Local\Packages\DISTRO_FOLDER\LocalState\rootfs

%userprofile%\AppData\Local\Packages

Ubuntu: => CanonicalGroupLimited.UbuntuonWindows_79rhkp1fndgsc
openSUSE Leap 42: => 46932SUSE.openSUSELeap42.2_022rs5jcyhyac
SUSE Linux Enterprise Server 12: => 46932SUSE.SUSELinuxEnterpriseServer12SP2_022rs5jcyhyac


apt update

apt install nginx git -y

# STOP

sudo killall -9 nginx

# START

nginx
