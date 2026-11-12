# EFI for Dell Precision 5820

This repository contains an OpenCore EFI configuration for booting macOS Catalina on a Dell Precision 5820 workstation. Do not forget to generate a valid serial with GenSMBIOS. 

## Overview

The EFI is organized as a standard OpenCore layout:

- `BOOT/` contains the bootloader stub (`BOOTx64.efi`)
- `OC/` contains the main OpenCore configuration and runtime files
  - `config.plist` — OpenCore configuration
  - `ACPI/` — ACPI patches and SSDTs
  - `Drivers/` — boot drivers
  - `Kexts/` — kernel extensions
  - `Tools/` — OpenCore utilities
  - `OpenCore.efi` — the OpenCore EFI binary

## Intended Use

This EFI is intended for use with a Dell Precision 5820 and a compatible Catalina installation. It is meant to be copied into a system EFI partition or used as a prebuilt EFI folder for a hackintosh setup.

## Important Notes

- Always back up your existing EFI before replacing or modifying it.
- Use this config as a starting point and verify hardware-specific settings for your exact machine.
- You may need to adjust SMBIOS, USB mapping, kexts, and ACPI patches depending on your installed hardware and macOS setup.
- This repository is not a full macOS installer; it provides the EFI files required to boot Catalina.

## Typical Setup

1. Prepare a USB installer or install macOS Catalina on compatible storage.
2. Mount your EFI partition.
3. Replace or merge the contents of the EFI partition with the files in this repository.
4. Boot with the OpenCore EFI and verify the system loads correctly.
5. Make adjustments as needed for your Dell Precision 5820 hardware configuration.

## Disclaimer

This project is provided for educational and troubleshooting purposes. Hackintosh setups can be hardware- and configuration-specific, and some settings may need to be customized for your machine.

## References

- OpenCore project: https://dortania.github.io/OpenCore-Install-Guide/
- macOS Catalina compatibility guidance and troubleshooting resources
