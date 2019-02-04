Networking
==========

.. contents:: **CONTENTS**
   :depth: 2

Networking for the Ultimate devices
----------------------------------

The Ultimate2+ and the Ultiamte64 have a built-in ethernet port which you can
use to connect the U2+ to your network or directly to your modern computer.

The Ultimate2 does not have an ethernet port, but it does have a USB port. You
can connect the U2 to your local network or modern computer using an USB2LAN
adapter. Any USB2LAN adapter that uses an AX88772/-A/-B chip should work.

The Ultimate64 also has a radio chip (ESP32) which is not yet used for
networking.

The Ultimate2+ is included in the Ultimate64, any reference to the Ultimate2+
in this document also concerns the Ultimate64.



Connect the Ultimate to your network
````````````````````````````````````

To connect the Ultimate cartridge to your network you will need an ethernet
cable. Connect the ethernet cable to your local network. Most likely you can
connect it to the switch of your modem/router. The modem/router will likely use
DHCP to serve your Ultimate cartridge an IP-address.

You can check and see if the Ultimate cart has a working network connection by 
checking the Net0 status in the Ultimate menu. You will see something like:

:: 

         *** Ultimate-II Plus 3.2a (110) 
  ──────────────────────────────────────────────
  Usb0    Lexar    USB Flash Drive     Ready
  Usb1    Lexar    USB Flash Drive     Ready
  Net0    IP: 192.168.2.64             Link Up
  
  
                                       ─F3=Help─
  /

For the U2+, when the link is down, it will show: 

:: 

         *** Ultimate-II Plus 3.2a (110)
  ──────────────────────────────────────────────
  Usb0    Lexar    USB Flash Drive     Ready
  Usb1    Lexar    USB Flash Drive     Ready
  Net0    MAC 01:21:3a:4f:64:6f        Link Down
  
  
                                       ─F3=Help─
  /

This means that when the link is down the U2+ will show its MAC address. If the
security policies of your modem/router needs the MAC address in order to serve
anydevice on your network an IP address, then use this address.

On the U2 I believe that when there is no USB2LAN adapter connect, there will
be no message shown at all. It will only show this information only when the
USB2LAN adapter is connected.

Using a direct connection
`````````````````````````
If you don't have the means to connect your Ultimate cartridge to a
modem/router, you can connect the Ultimate cartridge directly to your modern
computer. This means that you can only reach the Ultimate cart from this
computer and not from other devices on your network (better security).

To configure such a direct connection, you will need to configure your Ultimate cartridge to something like this: 

::

     *** Ultimate-II Plus 3.2a (110) ***   
  ┌───────────────────────────────────────┐
  │Use DHCP                       Disabled│
  │Static IP                   64.64.64.64│
  │Static Netmask            255.255.255.0│
  │Static Gateway                         │
  │Host Name                           U2P│
  │                                       │
  │                                       │
  │                                       │
  └───────────────────────────────────────┘
   /                             –F3=Help– 
  

You will also need to configure the ethernet network connection for your modern
computer. To connect to the Ultimate cart, you will need to use a different
IP-address, but you will need to use the same net mask. E.g. IP-address:
64.64.64.65 and Netmask: 255.255.255.0. Note that in this example you should
only change the last number in the IP-address.

Make sure to make a note of the IP-address. You will need this address to reach
the Ultimate cartridge on the network.


Using the network connection
----------------------------
At the time of writing there are 4 applications:

1) remote control (using telnet)
2) file transfer (using FTP)
3) using tcp port 64 (raw socket)
4) accessing the network / internet from the C64 (UCI)


Remote control 
``````````````
It is possible to completely control the Ultimate cart via a network
connection. You will need a telnet application to do so. I will not go into
details on how to configure your telnet application. Most standard telnet
applications will work out-of-the-box with recent firmware releases.

Modern operating systems usually do not come with a standard telnet client.
This means that you will need to install a telnet client yourself. You can use
your favourite package manager. On macOS you can use homebrew (https://brew.sh)
and simply type 'brew install telnet'. The telnet client is started from the
command line. For Microsoft Windows Operating System you can use `PuTTY
<https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html>`_ (`https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html <https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html>`_)

Please make sure that your telnet / terminal client supports vt100. The
Ultimate remote screen operates at 60 columns by 24 rows.

To connect to your Ultimate cartrdige simply type on the commandline of your
modern computer.

- telnet <ip-address>

e.g. 

- telnet 192.168.2.64
- telnet 64.64.64.64

If you use Microsoft Windows Operating System, open your telnet client and make
sure to type the ip address in the 'host' input field of your telnet client
before making a connection.

Once you're logged in, the screen will look like this:

::

         *** Ultimate-II Plus 3.2a (110) *** Remote ***       
  ────────────────────────────────────────────────────────────
  Usb1    Lexar    microSD RDR                       Ready    
  Usb0    Lexar    USB Flash Drive                   Ready    
  Net0    IP: 192.168.2.64                           Link Up  
  
  
  
                                                              
  /                                                  ─F3=Help─

Once you are connected to the 'remote menu' you can fully operate the the U2
and U2+ like you're used to do using the Ultimate menu on your C64.


File transfer (using FTP)
`````````````````````````

To transfer files from and to the Ultimate cartridge you can use the file
transfer protocol, also know as FTP.

The easiest way to use FTP is use one of the many FTP-clients.

**Windows:**
* Filezilla
* winscp
...

**Mac:**
* Filezilla
* duckuck
...

