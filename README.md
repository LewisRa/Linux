# Linux

C Drive
Program Files where's the directory that Linux is installed in 

Windows and Linux evolved in very different ways.Once upon a time there was a thing called ms-dos the disk operating system
it was command-line only but you could still run programs games and WordPerfect but you didn't need Windows. Windows was added to PCs and you can install it on top of DOS you would start up your computer and type in win to start
**Windows kernel** 

Linux follows UNIX traditions which is why uses the forward slash instead of the back slash like Windows.  Linux also cares
about capitalization so you can have things like File, file, FILE fIle
FiLe, fiLE as you can see while they're all named file they all use different
capitalization so Linux will allow this because they're technically not named
exactly the same 

Mac users who have explored their hard drives might find Linux a little more familiar this is because Mac's also evolved from a UNIX
ancestor more specifically BSD. 

**filesystem hierarchy standard or FHS defines the
structure and layout and is maintained by the Linux Foundation**
/bin (binaries) these are the most basic binaries which is another word for programs or applications things like LS
to list your directory  OR cat to display the output of a file and other basic functions are stored here.

sbin are system binaries that a system administrator would use and that a standard user wouldn't have access to without permission
both of these folders contain the files that need to be accessible when running
in single user mode as opposed to the usual multi-user mode.

single user mode
is a special mode that boots you in as a root user to allow you to do system
repairs and upgrades or testing networking is usually disabled in this
mode because of security issues when you install a program in Linux it's
typically not placed in these folders 

/boot is a folder you don't want to play around in it contains everything your OS needs to boot in other words your boot loaders live here. 

/dev this is where your devices live Linux. Following UNIX has a standard, everything is a file. In /dev, you will find your hardware. A disk,for example, would be /dev/sda and a partition on that disk would be for example /dev/sda1, /dev/sda2 etc. You can also find everything else here from your webcam to your keyboard. This is typically an area that applications and drivers will access and is rarely something a user should be dabbling in

/etc This folder is where all your system wide configurations are stored such as apt. In the  /etc/apt, for example, you would find the list of all your sources and repos your system connects to as well as its various settings so if you're
looking for something that is a system-wide application and not a per
user setting for example Libre Office would have settings in each user's
folder and it wouldn't be system-wide because each user can have different
settings.

/home

/lib folders (/lib, /lib32,/lib64) are where the libraries are stored. Libraries are files that applications can use to perform various functions. They're
required by the binaries in /bin and /sbin for example.

/media and /MNT(mount) are the directories are where you would find your other mounted drives. It can be a floppy disk, USB stick, external hard drive, network drive or, a second hard drive. The media folder wasn't always around it was
typically just MNT and that's where you mounted your storage devices.But now,  if you're mounting things manually use the MNT directory and leave the media 

/opt = optional folder which is usually where manually installed software from vendors resides. For example is a VPN software that you installed and the drivers foryour printer/scanner. Also used for installing software you've created yourself

/proc is where you'll find pseudo files that contain
information about system processes and resources. For example, every process will
have a directory here which contains all kinds of information on that process. For example, using id (2344) found in task manager, if you navigate to /proc/2344
you can see all kinds of pseudo files . Psuedo files are not  actually
files on the system. Psuedo files are the kernel's way of translating other information to appear as files. So, you can open the status file and it'll show me all kinds of information on that kernals process like the time it takes the processes to run.

/root is the root users home folder unlike a user's home folder. It
does not contain the typical directories inside and it does not reside in the
home director.You can store files here if you wish but you need root
permissions to access it. 

/run  runs in RAM which means that everything in it is gone when the system's rebooted or shut down. It's used for processes that
start early in the boot procedure to store runtime information that they use
to function.

/snap is where snap packages are stored and are mainly used
by Ubuntu 

/SRV is the service directory where service data is stored it'll probably be empty for you but if you run a server such as a web server or FTP server you would store the files that will be accessed by external users here this allows for better
security since it's at the root of the drive and it also allows you to easily
mount this folder from another hard drive

/sys (system folder) is a way to interact with the
kernel. This directory is similar to the run directory and it's not physically written to the disk it's created every
time the system boots up so you wouldn't store anything here and nothing gets
installed here TMP is of course a temp or temporary directory this is where
files are temporarily stored by applications that could be used during a
session one example is if you're writing a document in a word processor it will
regularly save a temporary copy of what you're writing here so that if the
application crashes it can look here to see if there's a recent saved copy that
you can recover

/USR folder is the user application space where applications will be
installed that are used by the user as opposed to the /bin directory is used by
the system and system administrator to perform maintenance it's also known as
the UNIX system resource and any applications installed here are
considered non-essential for basic system operation installed applications
will reside in one of several places here such as user bin user s bin or
local bin local Ben with their required library stored
in local user local Lib or user Lib 

most programs that are installed from source
code will end up in the local folders many larger programs will install
themselves into user share 

any installed source code such as the kernel source
and header files will go into the SRC directory this directory seems like a
confusing mess at first and while the directory structure and what goes where
is laid out in the FHS I mentioned earlier you'll still have to sometimes
look in other places to find things someone making a certain application
might not adhere to the standard and could just do what they want

/var is the variable directory which contains files and
directories that are expected to grow in size. For example, /var/crash holds
information about processes that have crashed /var/log contains log files for
both the system and many different applications which will constantly grow
in size as you use the system. You'll also find other things in here like
databases for mail and temporary storage for printer queues also known as the
spool. 

/home folder is where you store your personal files and documents. Each user has
their own home folder and each user can only access their own unless they use
admin permissions. Some users mount the home folder on a different drive or
different partition which allows you to reinstall your system and preserve your
files the home folder also contains many different directories which store your
application settings a hidden directory is simply one that starts with a period
Linux hides these by default you can view them in the file manager by
selecting show hidden files or by pressing ctrl H this is of course using
Nautilus in gnome and some file managers might be different PC man FM is also
press ctrl H to view hidden files if you're in the terminal and you list
files it'll only show you what is not hidden unless you specify - a for all
and now you can see all your hidden files these hidden directory store
things like cache some applications like a browser used to
store temporary files other applications might store thumbnails or information
that will be used over and over repeatedly 

then you have folders like
config and local which store individual application settings.
