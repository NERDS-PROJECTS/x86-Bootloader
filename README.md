# x86-Bootloader
A bootloader is an initial firmware/software that looks for an Operating System to boot from in the main secondary storage device, then hands over control to the kernel.

# Motivation behind the Project

In a bid to become chip independent from the current x86/ARM duopoly, there has been a concerted effort from multiple independent organisations to make custom chipsets that are not only open and cost-effective, but also fully customisable. This project was an effort to build up the skills necessary to start developing chips from the ground up, eventually targetting RISC-V. Reverse-engineering existing technology that works well will help replicate and improve functionality in the final product.

# Design of the Bootloader

As a bootloader is a critical piece of firmware that needs to run before it finds an OS to boot, the code needs to be lightweight and efficient. Assembly fits the bill perfectly for now, and we will be working on a Virtual Machine to avoid nuking perfectly good bare-metal machines. qemu is a very lightweight solution for Virtual Machines, but you can use VMWare or VirtualBox if so inclined, and our assembler of choice here is nasm.

Ideally we should be running Linux, but working on Windows and MacOS isn't a barrier at all. The tools can be installed easily, as they are all CLI.

- ## Linux

  - For Debian/Ubuntu distros or their derivatives
  > `sudo apt install nasm qemu`

  - For Arch distros or derivatives
  > `sudo pacman -S nasm qemu`

- ## Windows

  - [Install Windows Subsystem for Linux](https://www.windowscentral.com/how-install-wsl2-windows-10) and download Ubuntu from the Microsoft Store
  - Open WSL and type in
  > `sudo apt install nasm qemu`
  
- ## MacOS
  - 
  > `brew install nasm qemu`
