# Trying to run Linux on Samsung Galaxy Book 10.8

Sharing some experiences about running, more precisely trying to run, Linux on a Samsung Galaxy Book 10.8" x86 tablet.

TLDR: WiFi and touchscreen are not working. So avoid this tablet.

## What works

Basic functionality is working (kernel ??) :

* Keyboard
* Touchpad
* Adaptive brightness

I haven't tested much more than that.

What seems buggy :

* Touchscreen
* Screen orientation

What is not working :

* WiFi

To be tested :

* Webcam
* Gyroscope

## Customization of the tablet

The tablet configuration was like this :

    Samsung Galaxy Book 10.8
    Intel(R) Core(TM) m3-7Y30 CPU @ 1.00GHz
    4GB RAM
    64GB SSD
    10.8" touchscreen display
    + a cover keyboard

The tablet was delivered to me in the end of April 2019. It was saled on Ebay as used but never opened.

## Trying Linux Live

The computer came with _Windows 10 Home_ installed.

Download **Fedora 30 Workstation Live x86_64** and write it on an USB drive.

Here is the steps to boot from the USB drive :

* Boot the computer
* On the boot screen displaying Samsung Galaxy Book Logo press **F10**
* Choose the USB UEFI entry

Boot the usual Fedora live session :

* Screen is in portrait mode :
  * open a terminal
  * type "xrandr -o left"

Stop here, WiFi is not working at all. Touchscreen sometime kind of works, but not usable.

## Output from some commands

### sudo lshw -sanitize

    linux@tablet:~$ sudo lshw -sanitize > output/lshw.txt
    [sudo] password for linux:
    linux@tablet:~$

Soon.

### lsmod

    linux@tablet:~$ lsmod > output/lsmod.txt
    linux@tablet:~$

See the output in [output/lsmod.txt](output/lsmod.txt)
See the output with Fedora 31 in [output/lsmod_fedora31.txt](output/lsmod_fedora31.txt)

### lscpu

    linux@tablet:~$ lscpu > output/lscpu.txt

See the output in [output/lscpu.txt](output/lscpu.txt)
See the output with Fedora 31 in [output/lscpu_fedora31.txt](output/lscpu_fedora31.txt)

### cat /proc/cpuinfo

    linux@tablet:~$ cat /proc/cpuinfo > output/cpuinfo.txt
    linux@tablet:~$

Soon.

### cat /proc/meminfo

    linux@tablet:~$ cat /proc/meminfo > output/meminfo.txt
    linux@tablet:~$

Soon.

### dmesg

    linux@tablet:~$ dmesg > output/dmesg.txt
    linux@tablet:~$

See the output in [output/dmesg.txt](output/dmesg.txt).
See the output with Fedora 31 in [output/dmesg_fedora31.txt](output/dmesg_fedora31.txt)


### Thermal sensors 

    linux@tablet:~$ sensors > output/sensors.txt
    linux@tablet:~$

Soon.

## Other references

None. Or not yet found.