# CMPE283-assignment3

Q) Your assignment is to modify the CPUID emulation code in KVM to report back additional information when special CPUID leaf nodes are requested.

a) For CPUID leaf node %eax=0x4FFFFFFE:Return the number of exits for the exit number provided (on input) in %ecx. This value should be returned in %eax

b) For leaf nodes 0x4FFFFFFE, if %ecx (on input) contains a value not defined by the SDM, return 0 in all %eax, %ebx, %ecx registers and return 0xFFFFFFFF in %edx. 

c) For exit types not enabled in KVM, return 0s in all four registers.

# Answer


