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

    * [Kexts](https://dortania.github.io/OpenCore-Install-Guide/ktext.html#kexts)

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