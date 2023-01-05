# OC-EFI

This is an OpenCore EFI folder made for a HP ProDesk 400 G3 (A bit more like G2.5) SFF

Might as well work with later/diferent models with some edits (Once It Boots As of January 1 2022)

# OCSysInfo Output
<details>
  <summary>CPU</summary>
  
  - Intel(R) Core(TM) i3-6100 CPU @ 3.70GHz
    - SSE: SSE4.2
    - SSSE3: Supported
    - Cores: 2
    - Threads: 4
    - Codename: Skylake
</details>

<details>
  <summary>Motherboard</summary>
  
  - Model: 8062
  - Vendor: HP
</details>

<details>
  <summary>GPU</summary>
  
  - HD Graphics 530
    - Device ID: 0x1912
    - Vendor: 0x8086
    - ACPI Path: \_SB_.PCI0.GFX0
    - PCI Path: PciRoot(0x0)/Pci(0x2,0x0)
</details>

<details>
  <summary>Network</summary>
  
  - RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller
    - Device ID: 0x8168
    - Vendor: 0x10ec
    - ACPI Path: \_SB_.PCI0.RP05.PXSX
    - PCI Path: PciRoot(0x0)/Pci(0x1c,0x0)/Pci(0x0,0x0)
</details>

<details>
  <summary>Audio</summary>
  
  - 100 Series/C230 Series Chipset Family HD Audio Controller
    - Device ID: 0xa170
    - Vendor: 0x8086
    - ACPI Path: \_SB_.PCI0.HDAS
    - PCI Path: PciRoot(0x0)/Pci(0x1f,0x3)
    - Codec: ALC221
</details>

<details>
  <summary>Storage</summary>
  
  - Mass Storage Device
    - Type: Hard Disk Drive (HDD)
    - Connector: SCSI
    - Location: Internal
  - SanDisk Cruzer Blade
    - Type: Hard Disk Drive (HDD)
    - Connector: SCSI
    - Location: External
  - ATA WDC WD10EZEX-00B
    - Type: Hard Disk Drive (HDD)
    - Connector: SCSI
    - Location: Internal
</details>

# More Details
```
╭─ minerodo@minerodo-pc ~                                                                                                                                                                                                                                     
╰─❯ lspci
00:00.0 Host bridge: Intel Corporation Xeon E3-1200 v5/E3-1500 v5/6th Gen Core Processor Host Bridge/DRAM Registers (rev 07)
00:02.0 VGA compatible controller: Intel Corporation HD Graphics 530 (rev 06)
00:14.0 USB controller: Intel Corporation 100 Series/C230 Series Chipset Family USB 3.0 xHCI Controller (rev 31)
00:14.2 Signal processing controller: Intel Corporation 100 Series/C230 Series Chipset Family Thermal Subsystem (rev 31)
00:16.0 Communication controller: Intel Corporation 100 Series/C230 Series Chipset Family MEI Controller #1 (rev 31)
00:17.0 SATA controller: Intel Corporation Q170/Q150/B150/H170/H110/Z170/CM236 Chipset SATA Controller [AHCI Mode] (rev 31)
00:1c.0 PCI bridge: Intel Corporation 100 Series/C230 Series Chipset Family PCI Express Root Port #5 (rev f1)
00:1f.0 ISA bridge: Intel Corporation H110 Chipset LPC/eSPI Controller (rev 31)
00:1f.2 Memory controller: Intel Corporation 100 Series/C230 Series Chipset Family Power Management Controller (rev 31)
00:1f.3 Audio device: Intel Corporation 100 Series/C230 Series Chipset Family HD Audio Controller (rev 31)
00:1f.4 SMBus: Intel Corporation 100 Series/C230 Series Chipset Family SMBus (rev 31)
01:00.0 Ethernet controller: Realtek Semiconductor Co., Ltd. RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller (rev 15)
```

```
╭─ minerodo@minerodo-pc ~                                                                                                                                                                                                                                    
╰─❯ lsusb
Bus 002 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 001 Device 010: ID 12d1:107d Huawei Technologies Co., Ltd. SDM450-MTP _SN:90AE9CA0
Bus 001 Device 006: ID 0781:5567 SanDisk Corp. Cruzer Blade
Bus 001 Device 005: ID 0c45:5204 Microdia USB DEVICE
Bus 001 Device 004: ID 045e:00cb Microsoft Corp. Basic Optical Mouse v2.0
Bus 001 Device 003: ID 0bda:c811 Realtek Semiconductor Corp. 802.11ac NIC
Bus 001 Device 002: ID 14cd:6116 Super Top M6116 SATA Bridge
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
```

```
╭─ minerodo@minerodo-pc ~                                                                                                                                                                                                                                     
╰─❯ lscpu 
Architecture:            x86_64
  CPU op-mode(s):        32-bit, 64-bit
  Address sizes:         39 bits physical, 48 bits virtual
  Byte Order:            Little Endian
CPU(s):                  4
  On-line CPU(s) list:   0-3
Vendor ID:               GenuineIntel
  Model name:            Intel(R) Core(TM) i3-6100 CPU @ 3.70GHz
    CPU family:          6
    Model:               94
    Thread(s) per core:  2
    Core(s) per socket:  2
    Socket(s):           1
    Stepping:            3
    CPU(s) scaling MHz:  23%
    CPU max MHz:         3700.0000
    CPU min MHz:         800.0000
    BogoMIPS:            7399.70
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology n
                         onstop_tsc cpuid aperfmperf pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefet
                         ch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid ept_ad fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec 
                         xgetbv1 xsaves dtherm arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d arch_capabilities
Virtualization features: 
  Virtualization:        VT-x
Caches (sum of all):     
  L1d:                   64 KiB (2 instances)
  L1i:                   64 KiB (2 instances)
  L2:                    512 KiB (2 instances)
  L3:                    3 MiB (1 instance)
NUMA:                    
  NUMA node(s):          1
  NUMA node0 CPU(s):     0-3
Vulnerabilities:         
  Itlb multihit:         KVM: Mitigation: VMX disabled
  L1tf:                  Mitigation; PTE Inversion; VMX conditional cache flushes, SMT vulnerable
  Mds:                   Mitigation; Clear CPU buffers; SMT vulnerable
  Meltdown:              Mitigation; PTI
  Mmio stale data:       Mitigation; Clear CPU buffers; SMT vulnerable
  Retbleed:              Mitigation; IBRS
  Spec store bypass:     Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:            Mitigation; usercopy/swapgs barriers and __user pointer sanitization
  Spectre v2:            Mitigation; IBRS, IBPB conditional, RSB filling, PBRSB-eIBRS Not affected
  Srbds:                 Mitigation; Microcode
  Tsx async abort:       Not affected
```

```
╭─ minerodo@minerodo-pc ~                                                                                                                                                                                                                                     
╰─❯ sudo dmidecode -t baseboard
# dmidecode 3.4
Getting SMBIOS data from sysfs.
SMBIOS 2.7 present.

Handle 0x000D, DMI type 2, 17 bytes
Base Board Information
	Manufacturer: HP
	Product Name: 8062
	Version: KBC Version 05.39
	Serial Number: PEUDQ0JP1572CU
	Asset Tag:  
	Features:
		Board is a hosting board
	Location In Chassis:  
	Chassis Handle: 0x0000
	Type: Motherboard
	Contained Object Handles: 0

Handle 0x0011, DMI type 10, 6 bytes
On Board Device Information
	Type: Video
	Status: Enabled
	Description: 512 MB

Handle 0x0033, DMI type 41, 11 bytes
Onboard Device
	Reference Designation: Onboard IGD
	Type: Video
	Status: Enabled
	Type Instance: 1
	Bus Address: 0000:00:02.0

Handle 0x0034, DMI type 41, 11 bytes
Onboard Device
	Reference Designation: Onboard Lan
	Type: Ethernet
	Status: Enabled
	Type Instance: 1
	Bus Address: 0000:00:1f.6
```
