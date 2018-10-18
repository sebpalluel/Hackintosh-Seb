#### Hackintosh-Seb
Hackintosh config
### Guide

https://www.tonymacx86.com/threads/update-directly-to-macos-high-sierra.232707/
https://hackintosher.com/guides/updating-your-hackintosh-to-mojave-10-14/

## As a general rule, all non system kext go to Library/Extensions (use Kext Utility, not plain copy with finder) avoid System/Library/Extensions (new Apple rule)

## An additional copy of FakeSMC goes in /EFI/Clover/kexts/Other - you can put an Ethernet kext there as well

## External kext installed `kextstat | grep -v com.apple`

Index Refs Address            Size       Wired      Name (Version) UUID <Linked Against
   14    0 0xffffff7f80a89000 0x4000     0x4000     com.rehabman.driver.USBInjectAll (0.6.2) 6A9D456A-D1B1-316E-90CD-78E5B0002C5E <12 11 4 3>
   15    4 0xffffff7f80e56000 0x12000    0x12000    org.netkas.driver.FakeSMC (1759) 987B8DEE-6600-3463-BFFA-DF500771FA5B <11 7 5 4 3 1>
   16    2 0xffffff7f81784000 0x1f000    0x1f000    as.vit9696.Lilu (1.2.3) 9C714621-4E3B-37F7-9439-49FB5355317B <7 5 4 3 2 1>
   17    0 0xffffff7f817a3000 0xc000     0xc000     as.lvs1974.NvidiaGraphicsFixup (1.2.6) DE5F7EC7-0837-322C-9A53-BFACB5ACF10B <16 7 5 4 3 2 1>
   28    0 0xffffff7f82ac2000 0xd9000    0xd9000    as.vit9696.AppleALC (1.2.6) 7CCD3E13-609E-39E3-A3AB-6596F38B38AE <16 12 7 5 4 3 2 1>
   51    0 0xffffff7f8270b000 0x18000    0x18000    com.insanelymac.driver.AppleIntelE1000e (3.3.5) 9D1E2775-F6C2-A585-E806-42F3A5527FFC <50 12 5 4 3 1>
   52    0 0xffffff7f8109a000 0x8000     0x8000     com.insanelymac.AtherosE2200Ethernet (2.2.1) 64DD0A8F-6C61-3332-B6E8-59BD7B8C1CA6 <50 12 5 4 3 1>
   67    0 0xffffff7f811c6000 0x36a000   0x36a000   com.realtek.driver.RtWlanU (1830.2.b7) 7DF15DFD-23DF-3350-80FA-E220BB88350A <50 48 5 4 3 1>
   72    0 0xffffff7f80e95000 0x5000     0x5000     org.hwsensors.driver.CPUSensors (1759) 1204F31F-1308-3F9A-B509-0425FC789815 <15 7 5 4 3>
   77    0 0xffffff7f80e9c000 0x8000     0x8000     org.hwsensors.driver.ACPISensors (1759) FA4DF6C0-0D3A-3CE2-8569-0AB2C84053E7 <15 11 7 5 4 3>
   93    0 0xffffff7f80e6c000 0xe000     0xe000     org.hwsensors.driver.LPCSensors (1759) 46F77040-FA0F-3AEC-8330-E776B2D56C60 <15 12 11 7 5 4 3>
  107    0 0xffffff7f80b80000 0x5000     0x5000     com.Cycling74.driver.Soundflower (2) 2D779840-7439-31E5-8A66-D786C3F47B75 <83 5 4 3>
  108    0 0xffffff7f80e7d000 0x12000    0x12000    org.hwsensors.driver.GPUSensors (1759) ABDC14A9-7D25-3608-A129-A039C80468F6 <15 12 11 7 5 4 3>
  119    0 0xffffff7f82cf5000 0x24000    0x24000    jp.co.roland.RDUSB012FDev (1.5.2) 82EBD37F-EF2B-3769-A9ED-7B0A31812200 <83 48 5 4 3>
  120    2 0xffffff7f82d19000 0x636000   0x636000   com.nvidia.web.NVDAResmanWeb (10.1.8) B6F24A84-70A3-3153-BE9A-BE7F85CE7178 <117 102 85 12 7 5 4 3 1>
  121    0 0xffffff7f8334f000 0x199000   0x199000   com.nvidia.web.NVDAGM100HalWeb (10.1.8) 89B5051B-B2D1-3F2A-84F0-11F5521412D2 <120 12 4 3>
  123    0 0xffffff7f83577000 0xa3000    0xa3000    com.nvidia.web.GeForceWeb (10.1.8) 406C4483-F056-3173-9463-1BE0B7D3ECCD <122 120 102 85 12 7 5 4 3 1>
  130    0 0xffffff7f80ea9000 0x2000     0x2000     com.nvidia.CUDA (1.1.0) 4329B052-6C8A-3900-8E83-744487AEDEF1 <4 1>
  131    0 0xffffff7f8361a000 0x17000    0x17000    com.tuxera.filesystems.tufsfs.fusefs_txantfs (2015.11.5) D961CF7D-F98C-EE44-3AA8-175397F81CB3 <7 5 4 3 1>


#update nvidia driver when upgrading OS
https://github.com/Benjamin-Dobell/nvidia-update/blob/master/README.md

#revert from APFS to HFS+
https://www.techrepublic.com/article/how-to-revert-back-to-apples-hfs-from-apfs/
