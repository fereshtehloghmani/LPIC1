# LPIC1
** link: https://linux1st.com/1012-boot-the-system.html

## sysfs
 sysfs is a pseudo file system provided by the Linux kernel that exports information about various kernel subsystems, hardware devices, and associated device drivers from the kernel's device model to user space through 
 virtual files.[1] In addition to providing information about various devices and kernel subsystems, exported virtual files are also used for their configuration.

Sysfs is mounted under the /sys mount point

## dev
  udev (userspace /dev) is a device manager for the Linux kernel.

## dbus
  D-Bus is a message bus system, a simple way for applications to talk to one another. In addition to inter-process communication, D-Bus helps coordinate process lifecycle;

## proc directory
  This is where the Kernel keeps its settings and properties. This directory is created on ram and files might have write access (say for some hardware configurations). 

## some commands
lsblk
lsusb
lspci

## Loadable Kernel Modules
Linux like any other OS needs drivers to work with hardware. In Microsoft Windows, you need to install the drivers separately but in Linux, the system has most of the drivers built-in. But to prevent the kernel from loading all of them at the same time and to decrease the Kernel size, Linux uses Kernel Modules. Loadable kernel modules (.ko files) are object files that are used to extend the kernel of the Linux Distribution. 

lsmode  # -- its show all kernel driver(module)
rmmode  # -- for remove module
insmode # its need the complete address and use modprobe is the easy way
modprobe  modulename

## The Boot Process
 1 Motherboard Firmware does a PowerOnSelfTest
 2 Motherboard loads the bootloader
 3 Bootloader loads the Linux Kernel-based on its configs/commands
 4 The Kernel loads and prepares the system (root filesystem) and runs the initialization program
 5 Init program start the service, other programs, ... (web server, graphical interface, networking, etc.)
 
## Firmware: BIOS  -  UEFI 
   bios is old version and first need MBR
   UEFI is new version of firmware

 ## BootLoader (GRUB) 
 Bootloader initializes the minimum hardware needed to boot the system and then finds and runs the OS. &  initramfs

 ## kernel ring buffer --یک دیسکی کنار کرنل  که بتونه دیسک و تازه لود کنه و در نتیجه لاگ ها رو در بافر ذخیره میکنه 
 ## How access to these logs?
    dmesg  -- its show you all loges during os boot
    /var/log/dmesg


    

 
   
