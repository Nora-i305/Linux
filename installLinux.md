# Installing Linux on VMware  
## Creating a Virtual Machine  
### To install Linux on VMware:
    -  Select **File > New Virtual Machine**.  
    - Choose **Custom** and continue.  
    - Select your Linux distribution.  
    - Set the virtual machine name and storage location.  
    - Configure CPU cores and processors.  
    - Allocate RAM based on your requirements.  
    - Choose **Bridged Networking** if internet access is needed.  
    - Create a virtual disk and define its size.  
    - Complete the setup and click **Finish**.  
## Mounting the ISO File
### After creating the virtual machine:

* Open VM settings.
* Select **CD/DVD (SATA)**.
* Enable **Use ISO Image File**.
* Browse and select the Linux ISO file. 

## Installing Ubuntu

After powering on the VM:

1. Select **Install Ubuntu**.
2. Choose language and keyboard layout.
3. Select **Normal Installation**.
4. Configure disk settings and start installation.
5. Enter your location, username, and password.
6. Restart the system after installation completes.

# Note > Installation steps may vary depending on the Linux distribution.

## Linux Users

* `$` indicates a regular user.
* `#` indicates the root (administrator) user.  

## VMware Tools

To install VMware Tools:

* Right-click the virtual machine and select **Install VMware Tools**.
* VMware Tools improve performance, file sharing, and screen resizing.

## Basic Commands

```bash
ls
```

List files and directories.

```bash
cd
```

Move to the user's home directory.

```bash
cd directory_name
```

Change to a specific directory.

```bash
Tab
```

Auto-complete files and directory names.

```bash
cd
```

Clear the terminal screen.

# Installing Linux on Hyper-V

## Creating a Virtual Machine

To install Linux on Hyper-V:

1. Open **Hyper-V Manager**.
2. Select **New > Virtual Machine**.
3. Enter a name for the virtual machine.
4. Choose a storage location if needed.
5. Select **Generation 2**.
6. Allocate the required amount of RAM.
7. Select a **Virtual Switch** for networking.
8. Create a virtual hard disk (VHDX).
9. Choose **Install an operating system from a bootable image file**.
10. Select the Linux ISO file.
11. Review the settings and click **Finish**.

## Installing Linux

1. Right-click the virtual machine and select **Connect**.
2. Click **Start**.
3. Boot from the ISO image.
4. Follow the Linux installation wizard.
5. Configure language, keyboard, username, and password.
6. Restart the system after installation.

# Installing Linux Using WSL

## Prerequisites

Before installing WSL, make sure:

1. System Location is set to **United States (US)**.
2. Use a VPN if network restrictions exist.
3. Hardware Virtualization is enabled in BIOS/UEFI.
4. **Windows Subsystem for Linux (WSL)** is enabled.
5. **Hyper-V** is enabled.
6. **Containers** feature is enabled.

## Change System Location

```text
Control Panel
→ All Control Panel Items
→ Region
→ Location
→ United States
```

## Enable WSL

Open PowerShell as Administrator:

```powershell id="1z0a65"
wsl --install
```

Restart the system after installation.

## Install a Linux Distribution

List available distributions:

```powershell id="s8ubpa"
wsl --list --online
```

Install Ubuntu:

```powershell id="nmnajg"
wsl --install -d Ubuntu
```

After installation, create a Linux username and password.

## Verify Installation

```powershell id="rtphf9"
wsl --status
```

Display WSL status.

```powershell id="w2fgx5"
wsl -l -v
```

Display installed distributions.  
