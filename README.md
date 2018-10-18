# Hackintosh-Seb
Hackintosh config
## Guide

https://www.tonymacx86.com/threads/update-directly-to-macos-high-sierra.232707/
https://hackintosher.com/guides/updating-your-hackintosh-to-mojave-10-14/

### As a general rule, all non system kext go to Library/Extensions (use Kext Utility, not plain copy with finder) avoid System/Library/Extensions (new Apple rule)

### An additional copy of FakeSMC goes in /EFI/Clover/kexts/Other - you can put an Ethernet kext there as well

### External kext installed `kextstat | grep -v com.apple`


#### update nvidia driver when upgrading OS
https://github.com/Benjamin-Dobell/nvidia-update/blob/master/README.md

#### revert from APFS to HFS+
https://www.techrepublic.com/article/how-to-revert-back-to-apples-hfs-from-apfs/
