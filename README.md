# Linux-Mint-on-Dell-XPS-13-9310-
How to get all working when installing Linux Mint on Dell XPS 13 (9310)

I have tried Ubuntu, Arch Linux, Manjaro and Linux Mint on this Laptop and, in my opinion, Linux Mint is the better and most stable Linux distro for this laptop.

My laptop has the wifi card AX500, that is the most conflictive hardware for Arch distros. 

Since the laptop has the [certificate](https://ubuntu.com/certified/202007-28063) from Ubuntu, I think is a good decision use an Ubuntu based distribution for better stability. So, Ubuntu, Linux Mint, MX Linux, Elementary OS,... would be good options and the installation will be like this. 

Let's start the tutorial:

1.  [Download](https://linuxmint.com) and install Linux Mint using the last ISO and [Rufus](https://rufus.ie/en/) for create the bootable USB.

2.  After the install, WIFI and other hardware will not work. You need to connect to Internet with a wire connection (f.e. with your smartphone).

3.  Download and install [from here](http://archive.ubuntu.com/ubuntu/pool/main/l/linux-meta-oem-5.6):

          linux-headers-oem-20.04_5.6.0.1007.7_amd64.deb
          
          linux-image-oem-20.04_5.6.0.1007.7_amd64.deb
          
          linux-tools-oem-20.04_5.6.0.1007.7_amd64.deb
          
          linux-oem-20.04_5.6.0.1007.7_amd64.deb

4.  Download and install [from here](http://archive.ubuntu.com/ubuntu/pool/main/l/linux-firmware/):

          linux-firmware_1.199_all.deb
          
5.  After that, add repositories:

          sudo nano /etc/apt/sources.list.d/somerville-dla-team-ubuntu-ppa-bionic.list
      
And paste this:

          deb http://ppa.launchpad.net/somerville-dla-team/ppa/ubuntu bionic main
          # deb-src http://ppa.launchpad.net/somerville-dla-team/ppa/ubuntu bionic main
          # deb-src http://ppa.launchpad.net/somerville-dla-team/ppa/ubuntu bionic main
         
Also:
               
         sudo nano /etc/apt/sources.list.d/focal-oem.list
           
And paste this:

          deb http://oem.archive.canonical.com/ focal oem
          #deb-src http://oem.archive.canonical.com/ focal oem
          
And also:

          sudo nano /etc/apt/sources.list.d/oem-somerville-bulbasaur-meta.list
          
And paste this:

          deb http://dell.archive.canonical.com/ focal somerville
          # deb-src http://dell.archive.canonical.com/ focal somerville
          deb http://dell.archive.canonical.com/ focal somerville-bulbasaur
          # deb-src http://dell.archive.canonical.com/ focal somerville-bulbasaur
