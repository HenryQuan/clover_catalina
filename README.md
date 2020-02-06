# Clover Catalina
Catalina 10.15.2 clover config for Z390I AORUS PRO WIFI

## Configuration
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

### Storage
![screenshot from mac os](https://raw.githubusercontent.com/HenryQuan/clover_catalina/master/assets/storage.png)
#### SSD - System
- 128GB for Mac OS Catalina
- 372GB for Windows 10 pro
#### HDD - Storage
- Formatted as `exFAT`
- 256GB for `TimeMachine`
- File sharing between Windows and Mac OS

*If you see `no enough space` while using disk utility, you have to create an `EFI` partition with at least `200MB` (199MB won't work). Also, it might be better to install Mac OS first and then install Windows*

## How to install
- Check [this guide](https://www.tonymacx86.com/threads/unibeast-install-macos-catalina-on-any-supported-intel-based-pc.285366/) for preparation on tonymacx86 and use it as a generic guide
- [Guide](https://github.com/shiruken/hackintosh) by shiruken for Z390I
- [Guide](https://github.com/icymind/hackintosh) by icymind for Z390I

## Extra
- You will need to use config_installer.plist during your installation and system updates
- `Clover Configuration` and `Hackintool` are recommended
- Remember to install kexts with `Hackintool`
- I couldn't get it to work with Intel Graphics only (no egpu), the best `ProductName` was macmini for me but flickering didn't stop (other names will just show a green screen
- Sadly, I had to change to an AMD card to make it work
- Wait patiently for `Time Machine` to setup
- Nvidia cards won't work and don't even try it (for high sierra and below only)
- I used `Turbo Boost Swicther` to disable intel turbo boost
- GPU is quite cool without any power management
