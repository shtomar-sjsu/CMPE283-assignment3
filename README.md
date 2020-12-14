# CMPE283-assignment3

Q) Your assignment is to modify the CPUID emulation code in KVM to report back additional information when special CPUID leaf nodes are requested.

a) For CPUID leaf node %eax=0x4FFFFFFE:Return the number of exits for the exit number provided (on input) in %ecx. This value should be returned in %eax

b) For leaf nodes 0x4FFFFFFE, if %ecx (on input) contains a value not defined by the SDM, return 0 in all %eax, %ebx, %ecx registers and return 0xFFFFFFFF in %edx. 

c) For exit types not enabled in KVM, return 0s in all four registers.

# Answer

It should have a complete of Assignment-2 like below

1) Have VMFusion full setup with Ubuntu ISO image

2) It should have Linux kernal downloaded from github

3) Clone the kernel sources from the master Linux git repository:
git clone https://github.com/torvalds/linux.git

4) Build the kernel, Install packages necessary to compile the Linux kernel from source:

5) Modify the kernel code with the assignment functionality: ◦

6) After changing the file , both in vmx.c and Cpuid.c file, compile it with *make*

7) By installing virtmanager, create a InnerVM with ubuntu ISO image and install cpuid package on ubuntu in inner VM

8) Create a user-mode program that performs various CPUID instructions required to test this assignment.

9) Following is the output

<img width="837" alt="output1" src="https://user-images.githubusercontent.com/71058994/102035806-3932d500-3d76-11eb-9731-9d1748359bd9.png">


=====================================================================================

1) Comment on the frequency of exits – does the number of exits increase at a stable rate? Or are there more exits performed during certain VM operations? Approximately how many exits does a full VM boot entail?

<img width="835" alt="output2" src="https://user-images.githubusercontent.com/71058994/102035918-7dbe7080-3d76-11eb-91ae-d83cf23d5c0f.png">

2) Of the exit types defined in the SDM, which are the most frequent? Least?


======================================================================================

1) Shivam Tomar(SJSU ID: 015218203) 

    Modified cpuid.c & vmx.c files according to assignment-3, Added nested virtualisation, Tested output

2) Srujana Koripalli(SJSU ID: 013859651)

    Reasearched which code can be modified and what required for assignment-2 . Tested Output 
