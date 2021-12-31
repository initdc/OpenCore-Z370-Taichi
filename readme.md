# OpenCore-Z370-Taichi

> The OpenCore config for ASRock Z370 Taichi

## Working hardware

- CPU: i7-8700K
- MainBoard: ASRock Z370-Tacihi
- GPU Card: GTX1080Ti

## Working version

- OpenCore 0.6.7
- macOS 10.13.6

## Working features

- Broadcom Wi-Fi
- AirDrop
- Broadcom Bluetooth
- Nvidia HDMI

## Not Working features

- iGPU HDMI and DP
- Nvidia GPU DP

## Keypoint config

config.plist
```shell
# DevicesProperties >
# PciRoot(0x0)/Pci(0x2,0x0)
# i7-8700K
AAPL,ig-platform-id     00001259
device-id               12590000

# PlatformInfo > Generic
# macOS 10.13+
System Product Name     iMac18,3 

# NVRAM >
# 7C436110-AB2A-4BBB-A880-FE41995C9F82
# Disable kext signing for 10.13
csr-active-config       FF030000 

# UEFI > APFS
MinDate -1      MinVersion  -1
```

## Thanks to 

- The [OpenCore](https://github.com/acidanthera/OpenCorePkg) Project and its team

- The [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/troubleshooting/extended/post-issues.html#disabling-sip) # Disabling SIP

- Hackintosher forum [[Partially Solved] Issues With i7-8700K’s iGPU On High Sierra 10.13.6](https://hackintosher.com/forums/thread/partially-solved-issues-with-i7-8700k%E2%80%99s-igpu-on-high-sierra-10-13-6.10247/)