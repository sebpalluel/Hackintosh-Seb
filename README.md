# Hackintosh-Seb
Hackintosh config
## Guide

Install 3rd party kexts
https://www.tonymacx86.com/threads/guide-installing-3rd-party-kexts-el-capitan-sierra-high-sierra-mojave-catalina.268964/

https://www.tonymacx86.com/threads/update-directly-to-macos-high-sierra.232707/
https://hackintosher.com/guides/updating-your-hackintosh-to-mojave-10-14/

### As a general rule, all non system kext go to Library/Extensions (use Kext Utility, not plain copy with finder) avoid System/Library/Extensions (new Apple rule)

### An additional copy of FakeSMC goes in /EFI/Clover/kexts/Other - you can put an Ethernet kext there as well

### External kext installed `kextstat | grep -v com.apple`


#### update nvidia driver when upgrading OS
https://github.com/Benjamin-Dobell/nvidia-update/blob/master/README.md

#### revert from APFS to HFS+
https://www.techrepublic.com/article/how-to-revert-back-to-apples-hfs-from-apfs/

### Kexts
- FakeSMC : https://bitbucket.org/RehabMan/os-x-fakesmc-kozlek/downloads/
- Lilu : https://github.com/acidanthera/Lilu/releases
- WhateverGreen, AppleALC : https://github.com/acidanthera/Lilu/blob/master/KnownPlugins.md
- USBinjectAll : https://bitbucket.org/RehabMan/os-x-usb-inject-all/downloads/
