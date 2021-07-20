<p align="center">
	<img src="https://iili.io/JCfJ3u.png" width="200" height="48"/>
</p>

-----
# NOTE: i will not update OpenCore for this machine anymore
-----
[![OpenCore](https://img.shields.io/badge/OpenCore-0.6.8-blue)](https://github.com/acidanthera/OpenCorePkg)
![Support-status](https://img.shields.io/badge/Support-YES-Green)
![BigSur-support](https://img.shields.io/badge/BigSur-YES-Green)

<img align="right" src="https://user-images.githubusercontent.com/54585187/115138021-ca32f900-a053-11eb-915e-15046587e727.png" alt="Critter" width="550">

<img align="right" src="https://user-images.githubusercontent.com/54585187/115138031-dcad3280-a053-11eb-872d-ba518692939a.png" width="550">

<img align="right" src="https://user-images.githubusercontent.com/54585187/115138055-fea6b500-a053-11eb-9563-4a1b34c20839.png" width="550">

# Hackintosh Dell inspiron 3458
## macOS supported: High Sierra, Mojave, Catalina, BigSur

## Download [here](https://github.com/KhaiZeRoFX/OpenCore-Dell-inspiron-3458/releases "vv")
## Laptop Specs
- Intel Core i3 5005u (Broadwell)
- GPU intel HD 5500
- Ram 4GB
- Intel AC3160 (replaced with DW1820a)
- Audio ALC 255
- Ethernet RTL8106E
## Working
- Wifi 
- Native Power Management
- Bluetooth
- USB ports
- Battery status
- Keyboard & TrackPad
- Internal Audio & Microphone
- Headphone Jack
- HDMI Port (HDMI Audio)
- Graphics (Brightness Control Fn+B Fn+S)
- Sleep/Wake
- Ethernet
- Battery
- Bluetooth
- Icloud/Facetime/imessage
## Not Working
- etc
## Known issue
- [Remapping Fn+B Fn+S to F11 F12](https://github.com/KhaiZeR0/Hackintosh-Dell-inspiron-3458/blob/master/README.md#remapping-fnb-fns-to-f11-f12)

# macOS BigSur confirmed:

![oke](https://user-images.githubusercontent.com/54585187/91718709-22e57c80-ebbe-11ea-9d2b-9820924de92f.png)

### For Big Sur 11.4: Set xhciportlimit to FALSE

## Before Continue Guide!!

Please use ProperTree for customize config file

(Don't use OpenCore Configuration, Clover Configuration or it will broke your config file)

## Pre Condition

**Bios configuration**
Bios Config | Setting 
:---:| :---:
Intel SpeedStep | Enabled
Virtualization    | Enabled
USB Wake Support | Disabled
SATA Operation | AHCI

## 1. Change DVMT settings (already patched with 32mb dvmt on config)

Update your Bios to Lastest

1. Format USB as Fat32 and Copy EFI shell into it (Change EFI Shell name into EFI)

2. Boot with USB

3. At the grub prompt, enter these commands, hit enter after command, then exit and reboot

  `Setup_var 0x15B 0x3`
  
  `Setup_var 0x15C 0x3`
  
  ## *And now you have successfully changed the DVMT settings and fixed the kernel panic for graphics*
  
  ## 2. Create OSX Installer
  (I will use Olarila Mojave)
  
  *note: i do not recommended using Olarila to install because mine cause alot of issue with it and i reccommended using REAL vanilla on Apple AppStore or  Dortania OpenCore guide*
  
  1. Download MacOS Mojave From Olarila [here](https://drive.google.com/file/d/11XOoe-3Dcgqy97SJ3DGPSTx9Nz3LJIff/view "Here")
  
  2. Download [this](https://www.balena.io/etcher/ "this")
 
 3. Extract the .raw image
 
 4. Open Etcher, select image, select Drive and flash (Use USB 16GB or higher)
 
 ![Etcher](https://user-images.githubusercontent.com/54585187/78206356-cc69fa00-74c8-11ea-87d4-f380bd9d2b66.gif)

## 3. Install OSX

1. When OC boot screen appears, choose Install OS mojave ... (i guess)

2. The system will then boot into the OS X Installer

3. For a new installation of OS X, you MUST erase and format the destination drive according to the following steps before continuing.

   a. From the menu bar, click Utilities -> Choose Disk Utility
   
   b. Highlight your target hard drive for the High Sierra installation in left column.
   
   c. Click Erase tab
   
   d. Under Scheme: GUID Partition Map
   
   e. Under Name: type HD (You can name anything you want)
   
   f. Under Format: choose APFS
   
   g. Click Erase
   
   h. Close Disk Utility
   
4. Click Continue, Continue, Agree

5. Select name of your existing drive, where you want to install Macos Mojave and click Continue

6. Upon completion, system will restart

7. Press the F12 to choose boot device

8. Choose under UEFI Boot:

9. When OC boot screen appears, choose your existing name drive

10. After Booted successfull, copy your EFI folder from your USB to Hard drive and ready to go :)

# Remapping Fn+B Fn+S to F11 F12
Im trying to remap the Brigness Keyboard to F11 F12 but still got alot of issuse about BRT6 DSDT

You can use [Karabiner-Elements](https://karabiner-elements.pqrs.org) with this setting below

<img align="" src="https://user-images.githubusercontent.com/54585187/115134351-8e8b3580-a039-11eb-9e52-8fa5c865b74d.png" width="600">

# Wifi and bluetooth

Check it for more detail: [Wireless For Dell Inspiron 3458](https://github.com/KhaiZeR0/Wireless-For-Dell-Inspiron-3458)

[OpenCore Wireless Buyers Guide](https://dortania.github.io/Wireless-Buyers-Guide/)

# IMPORTANT:
(After installed MacOS sucessful, please change your System info with ProperTree and Clover configuration generate)

<img align="" src="https://user-images.githubusercontent.com/54585187/80679059-5caa5780-8ae6-11ea-9ded-beed34526b00.png" width="600">
<img align="" src="https://user-images.githubusercontent.com/54585187/80678840-ead20e00-8ae5-11ea-8f9e-128a9ed6e1c5.png" width="600">
<img align="" src="https://user-images.githubusercontent.com/54585187/80679145-806d9d80-8ae6-11ea-86d9-27d675b92a2a.png" width="600">


# ChimeBoot Sound

(If you are interesting in Chime sound on realmac, then just turn on it :>)
<img align="" src="https://user-images.githubusercontent.com/54585187/81152151-e016ed80-8fab-11ea-8574-5b0e665feef5.png" width="600">


## IF you wanna ask something: 
- [Opencore](https://dortania.github.io/OpenCore-Desktop-Guide/ "OpenCore") Guide
- [Olarila](https://www.olarila.com "Olarila") Website
- [Olarila](https://www.facebook.com/groups/122585311156411 "Olarila") Facebook group
- If you are VietNamese you can go to this [group](https://www.facebook.com/groups/224780132268974/?ref=share "group") and this [group](https://www.facebook.com/groups/hackintosh.vietnam "group")

# AND PLEASE 🙏 DO NOT USING THIS EFI FOR COMMERCIAL PURPOSES
## Credit
- [Apple](https://www.apple.com "Apple") for the Operation System
- [OpenCore](https://dortania.github.io/OpenCore-Desktop-Guide/misc/credit.html "OpenCore") for great Bootloader
- And for some other (i guess :v)
