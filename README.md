# HP Pavilion 550 Hackintosh

### This repo contains ready to use EFI to run macOS Big Sur on HP Pavilion 550（HP 畅游人 550）

EFI folder should work on other macOS versions, but it was only tested with Catalina and Big Sur


Model | HP Pavilion 550 (550-xxx) series
------------- | ---------------
CPU | Intel Core 6th/7th generation (For 7th gen, remember to upgrade BIOS from HP)
GPU | Intel UHD 630
RAM | 16GB DDR3 1600Mhz
Storage | Intel SSD 660p series
Software | macOS 11.2.3 Big Sur

## What works?

Everything works fine, with USB patched, but sleepinng doesn't work.

## Instalation

Download this repo. Generate SMBIOS data with [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) and set it in config.plist. Then copy to your EFI partition and that's it.

## What to expect

- Stable and reliable system, with USB ports patched!
- fully working sound including DP 
- Sleeping breaks, and I have no idea :(

## How to Install macOS Big Sur

There are two ways you can install Big Sur:

1. If you have an already working macOS, download the Installer from the App Store and make a bootable Installer with `createinstallmedia` by using this command in Terminal: `sudo /Applications/Install\ macOS\ Big\ Sur.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume`

2. If you are using Windows, use [macrecovery.py](https://github.com/acidanthera/OpenCorePkg/tree/master/Utilities/macrecovery) from the offical [OpenCore release package](https://github.com/acidanthera/OpenCorePkg/releases/). Follow this [guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/winblows-install.html) to understand how it works.

After you have created a bootable Installer, copy the EFI folder to the EFI partition and set SMBIOS data generated with [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS). Then install as usual. After the installation, mount the EFI partition of the installed OS and copy the EFI folder to its partition.
