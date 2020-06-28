# Clover Catalina
Catalina 10.15.2 clover config for Z390I AORUS PRO WIFI 

- ***it also works on 10.15.4 but you need to update clover***
- it also works on 10.15.5 but there are some issues with my display

# Configuration
||Name|
|:---:|:---:|
|Case|SliverStone Sugo SG13|
|Cooler|Noctua NH-L9i|
|CPU|Intel Core i5 9400|
|GPU|AMD Radeon RX 5700|
|HDD|Seagate BarraCuda 2TB 2.5"|
|Motherboard|Gigabyte Z390I AORUS PRO WIFI|
|Power|SilverStone SFX 500W|
|RAM|Corsair Vengeance 16GB (2x8GB) DDR4|
|SSD|Samsung 970 EVO Plus 500GB|

Two monitors + a keyboard + a mouse.

## What doesn't work
- WIFI
- Sidecar and all WIFI related features
- iMessage not tested and will never use it
- Microphone maybe (even with headphone)
- ~~Disk can be slow sometimes~~ (it is because of HDD)

## How to have WiFi
Download `HoRNDIS` and use `Android USB Tethering` but a dongle is better. 
Currently, I am using an `EDUP` dongle with [chris1111's driver](https://github.com/chris1111/Wireless-USB-Adapter-Clover). Yes, EDUP doesn't provide a driver for Catalina but chris1111's driver works really well.

I am not sure if the card can be changed or not. However, this build works great for me. 

## Storage
![screenshot from mac os](https://raw.githubusercontent.com/HenryQuan/clover_catalina/master/assets/storage.png)
### SSD - System
- 128GB for Mac OS Catalina
- 372GB for Windows 10 pro
### HDD - Storage
- Formatted as `exFAT`
- 256GB for `TimeMachine` (only 50GB left now)
- File sharing between Windows and Mac OS

It is recommended to turn off `RECYCLE BIN` on Windows because the HDD might not pass the `fsck_exfat` on Mac OS. Now, it is quite stable and I don't have to wait for a long time in order to use it.

*If you see `no enough space` while using disk utility, you have to create an `EFI` partition with at least `200MB` (199MB won't work). Also, it might be better to install Mac OS first and then install Windows*

# How to install
- Check [this guide](https://www.tonymacx86.com/threads/unibeast-install-macos-catalina-on-any-supported-intel-based-pc.285366/) for preparation on tonymacx86 and use it as a generic guide
- [Guide](https://github.com/shiruken/hackintosh) by shiruken for Z390I
- [Guide](https://github.com/icymind/hackintosh) by icymind for Z390I

# Extra
- You will need to use config_installer.plist during your installation and system updates
- `Clover Configuration` and `Hackintool` are recommended
- Use `MonitorControl` to adjust monitor volume and brightness
- Remember to install kexts with `Hackintool`
- I couldn't get it to work with Intel Graphics only (no egpu), the best `ProductName` was macmini for me but flickering didn't stop (other names will just show a green screen
- Sadly, I had to change to an AMD card to make it work
- Wait patiently for `Time Machine` to setup (it is only slow for the first backup)
- Nvidia cards won't work and don't even try it (for high sierra and below only)
- I used `Turbo Boost Swicther` to disable intel turbo boost
- GPU is quite cool without any power management (~~better than Windows 10~~ about the same now after some driver updates)
- ~~System update failed and maybe you need to switch back to Intel Graphics to make it work~~ Updated to 10.15.4 but I had no idea how. I think it failed because of clover and I simply updated to the latest version.
- Reinstalled Mac OS (10.15.5) and Windows 10 (2004) because Windows 10 2004 update messed up both of my system
  - Maybe don't do system update unless necessary
- Time Machine spent almost 4 hours to restore all my data but it works really well

