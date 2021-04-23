# CMPE 283 Assignment 1
### Yucong Ma 015244502



### Questions:
I did all the work for this assignment. Skip.

#### Steps to complete:
1. Install VMware fusion on my local machine
2. Install ubuntu on the VM
3. Install essential tools for git and gcc, etc.
4. Clone the linux repository.
5. Run ```make``` command
6. Run ```sudo insmod ./cmpe283-1.ko``` command
7. Run ```dmesg``` command. The output will be printed on the terminal console.
8. To repeat above steps, make sure to run ```sudo rmmod cmpe283-1``` in advance.

#### Sample output for the code

```
[   89.158626] CMPE 283 Assignment 1 Module Start
[   89.158642] Pinbased Controls MSR: 0x3f0000003f
[   89.158643]   External Interrupt Exiting: Can set=Yes, Can clear=No
[   89.158644]   NMI Exiting: Can set=Yes, Can clear=No
[   89.158645]   Virtual NMIs: Can set=Yes, Can clear=No
[   89.158645]   Activate VMX Preemption Timer: Can set=No, Can clear=Yes
[   89.158646]   Process Posted Interrupts: Can set=No, Can clear=Yes
[   89.158659] Procbased Controls MSR: 0xf5f9fffe9501e97a
[   89.158659]   Interrupt-window exiting: Can set=Yes, Can clear=Yes
[   89.158660]   Use TSC offsetting: Can set=Yes, Can clear=No
[   89.158661]   HLT exiting: Can set=Yes, Can clear=Yes
[   89.158661]   INVLPG exiting: Can set=Yes, Can clear=Yes
[   89.158662]   MWAIT exiting: Can set=Yes, Can clear=Yes
[   89.158662]   RDPMC exiting: Can set=Yes, Can clear=No
[   89.158663]   RDTSC exiting: Can set=Yes, Can clear=Yes
[   89.158663]   CR3-load exiting: Can set=Yes, Can clear=No
[   89.158664]   CR3-store exiting: Can set=Yes, Can clear=No
[   89.158664]   CR8-load exiting: Can set=Yes, Can clear=Yes
[   89.158665]   CR8-store exiting: Can set=Yes, Can clear=Yes
[   89.158666]   Use TPR shadow: Can set=Yes, Can clear=Yes
[   89.158666]   NMI-window exiting: Can set=Yes, Can clear=Yes
[   89.158667]   MOV-DR exiting: Can set=Yes, Can clear=Yes
[   89.158667]   Unconditional I/O exiting: Can set=Yes, Can clear=No
[   89.158668]   Use I/O bitmaps: Can set=No, Can clear=Yes
[   89.158668]   Monitor trap flag: Can set=No, Can clear=Yes
[   89.158669]   Use MSR bitmaps: Can set=Yes, Can clear=No
[   89.158669]   MONITOR exiting: Can set=Yes, Can clear=Yes
[   89.158670]   PAUSE exiting: Can set=Yes, Can clear=Yes
[   89.158683] Secondary Procbased Controls MSR: 0x111cfe00000000
[   89.158684]   Virtualize APIC accesses: Can set=No, Can clear=Yes
[   89.158684]   Enable EPT: Can set=Yes, Can clear=Yes
[   89.158685]   Descriptor-table exiting: Can set=Yes, Can clear=Yes
[   89.158685]   Enable RDTSCP: Can set=Yes, Can clear=Yes
[   89.158686]   Virtualize x2APIC mode: Can set=Yes, Can clear=Yes
[   89.158686]   Enable VPID: Can set=Yes, Can clear=Yes
[   89.158687]   WBINVD exiting: Can set=Yes, Can clear=Yes
[   89.158687]   Unrestricted guest: Can set=Yes, Can clear=Yes
[   89.158688]   APIC-register virtualization: Can set=No, Can clear=Yes
[   89.158688]   Virtual-interrupt delivery: Can set=No, Can clear=Yes
[   89.158689]   Pause-loop exiting: Can set=Yes, Can clear=Yes
[   89.158689]   RDRAND exiting: Can set=Yes, Can clear=Yes
[   89.158690]   Enable INVPCID: Can set=Yes, Can clear=Yes
[   89.158690]   Enable VM functions: Can set=No, Can clear=Yes
[   89.158691]   VMCS shadowing: Can set=No, Can clear=Yes
[   89.158691]   Enable ENCLS exiting: Can set=No, Can clear=Yes
[   89.158692]   RDSEED exiting: Can set=Yes, Can clear=Yes
[   89.158693]   Enable PML: Can set=No, Can clear=Yes
[   89.158693]   EPT-violation #VE: Can set=No, Can clear=Yes
[   89.158694]   Conceal VMX from PT: Can set=No, Can clear=Yes
[   89.158694]   Enable XSAVES/XRSTORS: Can set=Yes, Can clear=Yes
[   89.158695]   Mode-based execute control for EPT: Can set=No, Can clear=Yes
[   89.158695]   Sub-page write permission for EPT: Can set=No, Can clear=Yes
[   89.158696]   Intel PT uses guest physical address: Can set=No, Can clear=Yes
[   89.158697]   Use TSC scaling: Can set=No, Can clear=Yes
[   89.158697]   Enable user wait and pause: Can set=No, Can clear=Yes
[   89.158698]   Enable ENCLV exiting: Can set=No, Can clear=Yes
[   89.158710] VM-Exit Controls MSR: 0x3fffff00036dff
[   89.158711]   Save debug controls: Can set=Yes, Can clear=No
[   89.158712]   Host address-space size: Can set=Yes, Can clear=Yes
[   89.158712]   Load IA32_PREF_GLOBAL_CTRL: Can set=Yes, Can clear=Yes
[   89.158713]   Acknowledge interrupt on exit: Can set=Yes, Can clear=Yes
[   89.158713]   SAVE IA32_PAT: Can set=Yes, Can clear=Yes
[   89.158714]   Load IA32_PAT: Can set=Yes, Can clear=Yes
[   89.158714]   Save IA32_EFER: Can set=Yes, Can clear=Yes
[   89.158715]   Load IA32_EFER: Can set=Yes, Can clear=Yes
[   89.158715]   Save VMX-preemption timer value: Can set=No, Can clear=Yes
[   89.158716]   Clear IA32_BNDCFGS: Can set=No, Can clear=Yes
[   89.158717]   Conceal VMX from PT: Can set=No, Can clear=Yes
[   89.158717]   Clear IA32_RTIT_CTL: Can set=No, Can clear=Yes
[   89.158718]   Load CET state: Can set=No, Can clear=Yes
[   89.158718]   Load PKRS: Can set=No, Can clear=Yes
[   89.158731] VM-Entry Controls MSR: 0xf3ff000011ff
[   89.158732]   Load debug controls: Can set=Yes, Can clear=No
[   89.158732]   IA-32e mode guest: Can set=Yes, Can clear=Yes
[   89.158733]   Entry to SMM: Can set=No, Can clear=Yes
[   89.158733]   Deactivate dual monitor treatment: Can set=No, Can clear=Yes
[   89.158734]   Load IA32_PERF_GLOBAL_CTRL: Can set=Yes, Can clear=Yes
[   89.158734]   Load IA32_PAT: Can set=Yes, Can clear=Yes
[   89.158735]   Load IA32_EFER: Can set=Yes, Can clear=Yes
[   89.158735]   Load IA32_BNDCFGS: Can set=No, Can clear=Yes
[   89.158736]   Conceal VMX from PT: Can set=No, Can clear=Yes
[   89.158736]   Load IA32_RTIT_CTL: Can set=No, Can clear=Yes
[   89.158737]   Load CET state: Can set=No, Can clear=Yes
[   89.158737]   Load PKRS: Can set=No, Can clear=Yes
```