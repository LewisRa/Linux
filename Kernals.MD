# Kernals

Every multi-tasking computer system uses a kernel. Windows has a kernel, OS has a kernel,  iOS has a kernel and Android has a kernel. 
Windows useS a thing called the NT kernel OS 10 and iOS user thing called the Darwin kernel and Android uses the Linux kernel
Everything thing from a wearable and an IOT device right up to a the computer uses a kernel. 

The kernel is the thing manages the CPU resources: the memory, resources, and the processes on any computer. It also has device drivers in it so when
you want to do any networking that goes through the kernel like when we want to talk to Bluetooth that goes through the kernel. When
we want to use the file system that goes through the kernel. 

It is the lowest layer above the CPU. For example, on Android when you start an app, it is in fact the kernel that starts the
process for that app and enables the app to be loaded from the flash into memory if that app then needs some memory it
will be the kernel that will allocate it
to it if the app wants to do some
networking it will go through the kernel
is the app want to do something in the
background create a background service
that's handled by the kernel eventually
when the app closes that it all
resources that we use will be tidied up
and collected up by the kernel

There are actually some different ways in which kernels can be designed. The two main theories today for Codesign are what's called a **monolithic
kernel and a microkernel.** Linux is a monolithic kernel that means that all of these services that are going on all the
drivers or the stuff handling memory all occur inside one program that occupies one memory space 

The alternative is a thing called micro kernels and with micro kernels the kernel itself is in a very very small piece of memory space
and then other things like device drivers and networking and file system
drivers are running as user level
programs and the kernel talks of them
saying hey do this hey do that for me please go and get this file go and get that and they talk to the kernel the idea being that if one of those crashes the kernel itself doesn't crash 

As Linux kernel is a monolithic kernel, it can be quite big and complicated. There are 15 million lines of code in the Linux
kernel. Not all of that code is used all at once because in there there is support for IBM mainframes, a support for
PC, the support for SPARC processes, their support for ARM processors. There's a
whole range of different device drivers
in there in fact they say the 70% of
that 15 million lines of code is just
device drivers now when you build the
Linux kernel you say which bits you want
it's got a configuration program I want
this I don't want that I want this I
don't want that but you can do more than
just say what you want including what
you want execute you can also tweak the
way the operating system works and that
makes sense because if you're running
Linux on earth on a mainframe you might
want it to behave differently than if
you're running it on a wearable if
you're running it on a database server
you might want to do think differently
than if you're running it on a
smartphone and this is where we get into
the idea of custom kernels 

