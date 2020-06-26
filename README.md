# Locale Entry for macOS
macOS does not include any locale information for Indonesian language.
You need to include both directories listed here, *id_ID* and *id_ID.UTF-8*,
to enable support for Indonesian language.

# Prerequisite
For macOS 10.11 (El Capitan) and subsequent versions, you have to disable
[SIP](https://developer.apple.com/library/content/documentation/Security/Conceptual/System_Integrity_Protection_Guide/Introduction/Introduction.html)
(System Integrity Protection) by configuring it using the __csrutil(1)__ command.
First check whether SIP is currently enabled by running the following command
in the Terminal:
```
$ csrutil status
System Integrity Protection status: enabled.
```

To enable or disable SIP, you must boot into recovery mode and run the
__csrutil(1)__ command from the Terminal.
* Boot into recovery mode by restarting your machine and holding down the *Command* and *R*
keys at startup.
* Launch Terminal from the Utilities menu.
* Enter the command to disable SIP:
```
$ csrutil disable
```
Reboot is required after enabling or disabling SIP.

# Installation
* Copy both directories into  */usr/share/locale/*
* Change ownership of both directories, their subdirectories and files to *root:wheel*
* Boot into recovery mode by restarting your machine and reenabling SIP with the command:
```
$ csrutil enable
```
<br>
