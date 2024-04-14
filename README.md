# arm64-baremetal-course
A repo to setup a working environment for experimentation and lab exercises

```
The code provided as part of this repository is ONLY for learning purposes!
```

# TODO: Add course link

# Instructions
1. Setup your envrionment on Rpi (One time setup):
   1. Install raspbian on the Rpi and complete the installation
   2. Setup `ssh` on Rpi
   3. Install Kernel headers: `sudo apt install raspberrypi-kernel-headers`
2. Compile the kernel driver module
    1. Create a new folder e.g. `cd sample-assignment`
    2. Create necessary files and copy over the source code from the files attached in the course's assignment/lecture sections
    3. Once all the files are copied, your directory structure should contain - 
       1. Source - `.c` files for our Kernel driver
       2. Makefile - `Makefile`
    4. Run `make` to compile the kernel (You should see `module.ko` file being generated)
3. Install the module and validate the functionality
    1. Install the module: `sudo insmod <module_name.ko>`
    2. Verify the installation and working: `dmesg | tail -n 5`
    3. Uninstall the module: `sudo rmmod <module_name>`
    4. Can also check the list of all installed modules: `lsmod | grep <module_name>`

# Copyright

Copyright © 2024 inpyjama.com. All Rights Reserved.