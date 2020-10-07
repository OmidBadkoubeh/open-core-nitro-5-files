# Acer Nitro 5 (515-54) Open Core Files

---

# Preparation

## [Mandatory ACPI Files](#mandatory-acpi) [^1]

* [SSDT-PLUG (Power Management)](https://dortania.github.io/Getting-Started-With-ACPI/Universal/plug.html#fixing-power-management-ssdt-plug)

* [SSDT-EC/USBX (Embedded Controller)](https://dortania.github.io/Getting-Started-With-ACPI/Universal/ec-fix.html#fixing-embedded-controller-ssdt-ec-usbx)

* [SSDT-PNLF (BackLight)](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/backlight.html#fixing-backlight-ssdt-pnlf)

* [SSDT-GPI0/XOSI (Trackpad)](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/trackpad.html#fixing-trackpads-ssdt-gpi0-xosi)

* [SSDT-AWAC/RTC0 (System Clock)](https://dortania.github.io/Getting-Started-With-ACPI/Universal/awac.html#fixing-system-clocks-ssdt-awac-rtc0)

* [SSDT-PMC (NVRAM)](https://dortania.github.io/Getting-Started-With-ACPI/Universal/nvram.html#fixing-nvram-ssdt-pmc)

---

## Steps: 

1. [Make USB Installer](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/#making-the-installer)

2. [Adding The Base OpenCore Files](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/opencore-efi.html#adding-the-base-opencore-files)

3. [Gathering files](https://dortania.github.io/OpenCore-Install-Guide/ktext.html#gathering-files)

    * [Firmware Drivers](https://dortania.github.io/OpenCore-Install-Guide/ktext.html#firmware-drivers)

        - Universal

            * [`HfsPlus.efi`](https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi)

            * [`OpenRuntime.efi`](https://github.com/acidanthera/OpenCorePkg/releases) [^2]

    * [Kexts](https://dortania.github.io/OpenCore-Install-Guide/ktext.html#kexts)

        - Must Haves:

            * [`VirtualSMC`](https://github.com/acidanthera/VirtualSMC/releases)

            * [`Lilu`](https://github.com/acidanthera/Lilu/releases)

        - VirtualSMC Plugins:

            * `SMCProcessor.kext` : Used for monitoring CPU temperature

        - Graphics: 

            * [WhateverGreen](https://github.com/acidanthera/WhateverGreen/releases)

                - Note the `SSDT-PNLF.dsl` file included is only required for laptops and AIOs

        - Audio:

            * [AppleALC](https://github.com/acidanthera/AppleALC/releases)

        - Ethernet: 

            * [AtherosE2200](https://github.com/Mieze/AtherosE2200Ethernet/releases)

        - WiFi and Bluetooth:

            * [AX200 Wifi](https://github.com/OpenIntelWireless/itlwm/releases)

            * [Intel Bluetooth](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases)

        - Extras:

            * [NVMEFix](https://github.com/acidanthera/NVMeFix/releases)

        - Laptop Specifics: 

            * Input drivers: 

                - [VooDooSMBus](https://github.com/VoodooSMBus/VoodooSMBus) [^3]

                - [VooDooI2C](https://github.com/VoodooI2C/VoodooI2C/releases)

                - [AlpsT4USB](https://github.com/blankmac/AlpsT4USB)

                    * Used for USB ALPS devices, note this does **not** work with I2C based devices.

        - Misc:

            * [NoTouchID](https://github.com/al3xtjames/NoTouchID/releases)

                - Recommended for MacBook `SMBIOS` that include a TouchID sensor to fix auth issues, generally 2016 and newer `SMBIOS` will require this.

    * [SSDTs](https://dortania.github.io/OpenCore-Install-Guide/ktext.html#ssdts)

4. Make [ACPI Files](https://dortania.github.io/Getting-Started-With-ACPI/#getting-started-with-acpi) Mentioned [Here](#mandatory-acpi)

    * First try [manually built](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-long.html#ssdts-the-long-way) ACPI files

    * If does't work try [SSDTTime Generated](https://github.com/corpnewt/SSDTTime) files.

    * Avoid to use `Prebuilt ACPI` files.

5. [`config.plist` Setup](https://dortania.github.io/OpenCore-Install-Guide/config.plist/#config-plist-setup)

---

# Installation

1. [Enable BIOS settings optimal for macOS](https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html#installation-process)

    * Read up on the [Multiboot Guide](https://hackintosh-multiboot.gitbook.io/hackintosh-multiboot/)

1. [Double checking your work](https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html#double-checking-your-work)

2. [Booting the OpenCore USB](https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html#booting-the-opencore-usb)

3. [macOS Installer](https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html#macos-installer)

---

# [Post Install](https://dortania.github.io/OpenCore-Post-Install/#opencore-post-install)














---

[^1]: As they Recommended [here](https://dortania.github.io/OpenCore-Install-Guide/ktext.html#laptop)

[^2]: This file is in `Open Core` project files.

---

[x] - `VooDooSMBus.kext` & `AlpsT4USB`

[] - `VooDooI2C.kext`

---

