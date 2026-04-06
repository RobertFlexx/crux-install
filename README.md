## crux-install 3.8

Interactive installation script for CRUX[1] 3.8. It is completely text based
and assumes sane defaults. It speeds up CRUX installation by automating manual
steps while still allowing customization.

This enhanced fork improves usability while preserving the original minimal
design. It adds optional desktop environments (kde plasma and xfce), flatpak
support with flathub, improved partitioning, and updated CRUX 3.8 compatibility.

## install

```
(1) Boot from ISO

(2) Initialize network

    # dhcpcd

(3) Download install script

    # curl -LO https://raw.githubusercontent.com/akosela/crux-install/master/install

    (wget may not work in some environments, curl is recommended)

(4) Run it

    # sh install
```

## help

The install script will ask you several questions. The default answers (in [])
are sane and designed to install a working CRUX system with minimal effort.

```
Welcome to the CRUX 3.8 installation program.

(I)nstall, (U)pgrade, or (S)hell? [i]
```

Choosing the default answer [install] will perform a typical fresh
installation. You can choose to build your own kernel or copy it from another
system. When deploying multiple systems, copying a prebuilt kernel can save time.

The installer also provides optional features such as:

* Desktop environments (KDE Plasma 6 or Xfce)
* Flatpak with optional Flathub repository
* Improved auto-partitioning (including UEFI support)
* Simplified setup flow

The following questions are part of the install process:

```
System hostname? [crux]
Which network interface do you wish to configure? (or (N)one) [eth0]
IPv4 address for eth0? [dhcp]
What timezone are you in? [UTC]
(A)uto-partition or (F)disk? [a]
Which filesystem you want to use? ('?' for list) [ext4]
Size of the swap partition? (in MB) [1024]

Select desktop environment:
(0) None (minimal)
(1) KDE Plasma
(2) Xfce

Install Flatpak support? [y]

Your CRUX root partition has been mounted at /mnt.
Core packages only? [y]

Creating password for root account.
New password:

Please create a local account. [user]
New password:

Build your own kernel? [y]
Download custom .config? [n]

Your CRUX system is ready. Please reboot.
Exit to (S)hell, (H)alt, or (R)eboot? [r]
```

[1] http://crux.nu/
