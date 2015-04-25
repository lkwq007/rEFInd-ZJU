#Zhejiang University rEFInd theme

[The rEFInd Boot Manager](http://www.rodsbooks.com/refind/) is a simplistic boot manager for UEFI based systems. This is a rEFInd theme for the students of Zhejiang University. 

![Sreenshot-1](https://cloud.githubusercontent.com/assets/1665437/7332527/b29c655e-eb75-11e4-8176-bdb9e17c9aa4.png)![Sreenshot-2](https://cloud.githubusercontent.com/assets/1665437/7332526/abe61bba-eb75-11e4-8e6d-6289bac4b781.png)

##Usage

To use this theme you'll want to clone it into the same directory as your rEFInd efi executable (usually `EFI\refind\` in ESP for Windows, `/boot/EFI/refind/` for Linux). Then you will want to add the line `include rEFInd-ZJU/theme.conf` to the end of your `refind.conf`. 

To set the icons for your entries you will want to add the icon configuration to each menuentry which points to the icon under `rEFInd-ZJU/icons` that you would like to use for that entry. 

And here's an example configuration. 

```
menuentry "Ubuntu" {
	loader /EFI/ubuntu/grubx64.efi
	icon /EFI/refind/rEFInd-ZJU/icons/os_ubuntu.png
}

menuentry "Windows" {
    loader /EFI/Microsoft/Boot/bootmgfw.efi
    icon /EFI/refind/rEFInd-ZJU/icons/os_win.png
}

menuentry "OSX" {
    loader /EFI/Apple/Boot/bootmgfw.efi
    icon /EFI/refind/rEFInd-ZJU/icons/os_mac.png
}
```

Entries that are autodetected should also show the proper icons. 

##Attribution

The OS icons are from [Lightness for burg](http://sworiginal.deviantart.com/art/Lightness-for-burg-181461810) by [SWOriginal](http://sworiginal.deviantart.com/) and modified to be white. 

And I took the description of [rEFInd-minimal](https://github.com/EvanPurkhiser/rEFInd-minimal) as reference to write this description in English because my English is poor. 
