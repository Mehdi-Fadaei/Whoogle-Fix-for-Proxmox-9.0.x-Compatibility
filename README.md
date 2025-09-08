Whoogle-Fix-for-Proxmox-9.0.x-Compatibility
Updated pve_check() in whoogle.sh to allow Proxmox 9.0.x, fixing the version check so the script runs on 9.0.3 and later.
You can update your GitHub description or instructions like this:

Installing Whoogle on Proxmox 9 or Above

If you want to install Whoogle on Proxmox 9.x or later, the original script may fail due to the version check. To make it work:

1. Download both required files locally from this repository:


wget -O whoogle.sh https://raw.githubusercontent.com/Mehdi-Fadaei/Whoogle-Fix-for-Proxmox-9.0.x-Compatibility/main/whoogle.sh
wget -O build.func https://raw.githubusercontent.com/Mehdi-Fadaei/Whoogle-Fix-for-Proxmox-9.0.x-Compatibility/main/build.func


2. Make sure `whoogle.sh` sources the local `build.func` and are in root od Linux :

3. Run the script inside a Debian 12 or Ubuntu 22.04 LXC container:


bash whoogle.sh


✅ This will install Whoogle safely on Proxmox 9.x and avoid the “version not supported” error.

Note: Do not run the script directly on the Proxmox host—it must be inside a container.
