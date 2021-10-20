THis are very trimmed config files for the Dell D630.
The idea is leave behind a ton of code that either I do not use or is not needed for this particular hardware.
Of course YMMV, and this will most likely fail in your hardware :) Or not.
The benefits are hard to measure, if measurable at all.
Notice: Do not try to build you own kernel unless you either:
- Have a real issue, that you have learned can be fixed with a particular build.
- You have TONs of time, no boy/girl friend and you are willing to pull your hair for weeks before getting to a good result.
- You are curious to the point of willing to crash your machine, loose your data, and still comply with the above.

Also, added a quite trimmed config for this machine:
$ sudo lshw -short
[sudo] password for sjmuniz: 
H/W path            Device           Class          Description
===============================================================
                                     system         MS-7C95 (To be filled by O.E.M.)
/0                                   bus            B550M PRO-VDH (MS-7C95)
/0/0                                 memory         64KiB BIOS
/0/11                                memory         16GiB System Memory
/0/11/0                              memory         3600 MHz (0,3 ns) [empty]
/0/11/1                              memory         8GiB DIMM DDR4 Synchronous Unbuffered (Unregistered) 3600 MHz (0,3 ns)
/0/11/2                              memory         3600 MHz (0,3 ns) [empty]
/0/11/3                              memory         8GiB DIMM DDR4 Synchronous Unbuffered (Unregistered) 3600 MHz (0,3 ns)
/0/13                                memory         512KiB L1 cache
/0/14                                memory         4MiB L2 cache
/0/15                                memory         16MiB L3 cache
/0/16                                processor      AMD Ryzen 7 5700G with Radeon Graphics
/0/100                               bridge         Renoir Root Complex
/0/100/0.2                           generic        Renoir IOMMU
/0/100/2.1                           bridge         Renoir PCIe GPP Bridge
/0/100/2.1/0                         bus            Advanced Micro Devices, Inc. [AMD]
/0/100/2.1/0/0      usb1             bus            xHCI Host Controller
/0/100/2.1/0/0/4                     generic        802.11 n WLAN
/0/100/2.1/0/0/5                     input          USB Optical Mouse
/0/100/2.1/0/0/6                     input          USB Keyboard
/0/100/2.1/0/0/7                     bus            USB2.0 Hub
/0/100/2.1/0/0/8                     input          MYSTIC LIGHT
/0/100/2.1/0/1      usb2             bus            xHCI Host Controller
/0/100/2.1/0.1                       storage        Advanced Micro Devices, Inc. [AMD]
/0/100/2.1/0.2                       bridge         Advanced Micro Devices, Inc. [AMD]
/0/100/2.1/0.2/9                     bridge         Advanced Micro Devices, Inc. [AMD]
/0/100/2.1/0.2/9/0  enp42s0          network        RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller
/0/100/2.2                           bridge         Renoir PCIe GPP Bridge
/0/100/2.2/0                         storage        WD Black SN750 / PC SN730 NVMe SSD
/0/100/2.2/0/0      /dev/nvme0       storage        WDS500G3X0C-00SJG0
/0/100/2.2/0/0/1    /dev/nvme0n1     disk           500GB NVMe namespace
/0/100/2.2/0/0/1/1  /dev/nvme0n1p1   volume         99MiB Windows FAT volume
/0/100/2.2/0/0/1/2  /dev/nvme0n1p2   volume         15MiB reserved partition
/0/100/2.2/0/0/1/3  /dev/nvme0n1p3   volume         247GiB Windows NTFS volume
/0/100/2.2/0/0/1/4  /dev/nvme0n1p4   volume         520MiB Windows NTFS volume
/0/100/2.2/0/0/1/5  /dev/nvme0n1p5   volume         201GiB EXT4 volume
/0/100/2.2/0/0/1/6  /dev/nvme0n1p6   volume         16GiB Linux swap volume
/0/100/8.1                           bridge         Renoir Internal PCIe GPP Bridge to Bus
/0/100/8.1/0        /dev/fb0         display        Cezanne
/0/100/8.1/0.1                       multimedia     Advanced Micro Devices, Inc. [AMD/ATI]
/0/100/8.1/0.2                       generic        Family 17h (Models 10h-1fh) Platform Security Processor
/0/100/8.1/0.3                       bus            Renoir USB 3.1
/0/100/8.1/0.3/0    usb3             bus            xHCI Host Controller
/0/100/8.1/0.3/0/2                   multimedia     Logitech USB Headset
/0/100/8.1/0.3/1    usb4             bus            xHCI Host Controller
/0/100/8.1/0.4                       bus            Renoir USB 3.1
/0/100/8.1/0.4/0    usb5             bus            xHCI Host Controller
/0/100/8.1/0.4/0/1                   multimedia     HD Webcam C525
/0/100/8.1/0.4/1    usb6             bus            xHCI Host Controller
/0/100/8.2                           bridge         Renoir Internal PCIe GPP Bridge to Bus
/0/100/8.2/0                         storage        FCH SATA Controller [AHCI mode]
/0/100/8.2/0.1                       storage        FCH SATA Controller [AHCI mode]
/0/100/14                            bus            FCH SMBus Controller
/0/100/14.3                          bridge         FCH LPC Bridge
/0/101                               bridge         Renoir PCIe Dummy Host Bridge
/0/102                               bridge         Renoir PCIe Dummy Host Bridge
/0/103                               bridge         Renoir PCIe Dummy Host Bridge
/0/104                               bridge         Advanced Micro Devices, Inc. [AMD]
/0/105                               bridge         Advanced Micro Devices, Inc. [AMD]
/0/106                               bridge         Advanced Micro Devices, Inc. [AMD]
/0/107                               bridge         Advanced Micro Devices, Inc. [AMD]
/0/108                               bridge         Advanced Micro Devices, Inc. [AMD]
/0/109                               bridge         Advanced Micro Devices, Inc. [AMD]
/0/10a                               bridge         Advanced Micro Devices, Inc. [AMD]
/0/10b                               bridge         Advanced Micro Devices, Inc. [AMD]
/0/1                                 system         PnP device PNP0c01
/0/2                                 system         PnP device PNP0c02
/0/3                                 system         PnP device PNP0b00
/0/4                                 system         PnP device PNP0c02
/0/5                                 communication  PnP device PNP0501
/0/6                                 system         PnP device PNP0c02
/1                  wlx1ca0d3604095  network        Wireless interface

https://linux-hardware.org/?probe=b806a146d2

