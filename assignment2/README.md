# Assignment 2

This assignment is done by myself

# Steps to do the assignment

### Set up environment

1. Follow the steps in assignment 1 and install all necessary package

2. use ```uname -a``` to check current kernel version

![Output](/assignment2/oldkernel.jpg)

3. copy current kernel settings to linux repo by running ```cp -v /boot/config-5.4.0-43-generic ./.config```

4. run command ```make oldconfig```

5. run command to build linux kernel. ```make -j 4 && sudo make -j 4 modules && sudo make install && sudo make modules_install```

6. reboot after the command finished

7. check linux kernel version to make sure the new kernel is installed

![Output](/assignment2/newkernel.jpg)

### Modify kernel 

1. modify /arch/x86/kvm/cpuid.c to print out information and store value to corresponding register when eax set to 0x4fffffff

2. modify /arch/x86/kvm/svm/svm.c (For AMD cpu user only) to implement a counter for counting exits and recording cycle time.

3. build the module using command: ```sudo make modules SUBDIRS=arch/x86/kvm```

4. reload the module using command: ```sudo rmmod arch/x86/kvm/kvm-amd.ko && sudo rmmod arch/x86/kvm/kvm.ko && sudo insmod arch/x86/kvm/kvm.ko && sudo insmod arch/x86/kvm/kvm-amd.ko```

### Setup kvm inside VM

1. Install VM by running command ```sudo apt-get install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils```

2. Install Virtual manager ```sudo apt-get install virt-manager```

3. Install Ubuntu 20.04 in kvm

4. Run the test program in the kvm

### result

1. Test program output:

![Output](/assignment2/test.jpg)

2. From outer vm, check the kernel log by using command "dmesg"

![Output](/assignment2/dmesg.jpg)

### Questions

1. Does the number of exits increase at a stable rate? Or are there more exits performed during certain VM operations?

- Ans: NO, there are other exits caused by other instructions.

2. Approximately how many exits does a full VM boot entail?

- Ans: For my machine, it takes about 500000 exits for a full VM boot. This is the result from immediately open kvm and run the test script.

5. run command to build linux kernel. "make -j 4 && sudo make -j 4 modules && sudo make install && sudo make modules_install"

6. reboot after the command finished

7. check linux kernel version to make sure the new kernel is installed

### Modify kernel 

1. modify /arch/x86/kvm/cpuid.c to print out information and store value to corresponding register when eax set to 0x4fffffff

2. modify /arch/x86/kvm/svm/svm.c (For AMD cpu user only) to implement a counter for counting exits and recording cycle time.

3. build the module using command: "sudo make modules SUBDIRS=arch/x86/kvm"

4. reload the module using command: "sudo rmmod arch/x86/kvm/kvm-amd.ko && sudo rmmod arch/x86/kvm/kvm.ko && sudo insmod arch/x86/kvm/kvm.ko && sudo insmod arch/x86/kvm/kvm-amd.ko"

### Setup kvm inside VM

1. Install VM by running command "sudo apt-get install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils"

2. Install Virtual manager "sudo apt-get install virt-manager"

3. Install Ubuntu 20.04 in kvm

4. Run the test program in the kvm

### result

1. Test program output:

2. From outer vm, check the kernel log by using command "dmesg"

### Questions

1. Does the number of exits increase at a stable rate? Or are there more exits performed during certain VM operations?

- Ans: NO, there are other exits caused by other instructions.

2. Approximately how many exits does a full VM boot entail?

- Ans: For my machine, it takes about 500000 exits for a full VM boot. This is the result from immediately open kvm and run the test script.