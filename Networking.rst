Networking
----------

The Ultimate2+ and the Ultiamte64 have a built-in ethernet port which you can use to connect the U2+ to your network or directly to your modern computer.

The Ultimate2 does not have an ethernet port, but it does have a USB port. You can connect the U2 to your local network or modern computer using an USB2LAN adapter. Any USB2LAN adapter that uses an AX88772/-A/-B chip should work.

The Ultimate64 also has a radio chip (ESP32) which is not yet used for networking.

The Ultimate2+ is included in the Ultimate64, any reference to the Ultimate2+ also concerns the Ultimate64.



Connecting the Ultimate to the network
--------------------------------------
To connect the Ultimate cartridge to the network you will need an ethernet cable. Connect the ethernet cable to your local network. Most likely you can connect it to the switch of your modem/router. The modem/router will likely use DHCP to serve your Ultimate cartridge an IP-address.

You can check and see if the Ultimate cart has a working network connection by checking the Net0 status in the Ultimate menu. You will see something like:

Net0    IP:  192.168.2.64       Link Up

For the U2+, when the link is down, it will say something like: 

Net0    MAC  13:15:41:26:64:4f  Link Down

This means that when the link is down the U2+ will show its MAC address. If you have a modem/router that needs to mac address to have it serve an IP-address, then use this address. 

On the U2 I believe that when there is no working ethernet connection there is no message at at all. It will only show the link up line when the link is up.

If you don't have the means to connect your Ultimate cartridge to a modem/router, but have a free ethernet port on your modern computer, then you can connect the Ultimate cartridge directly to your modern computer. This means that you can only reach the Ultimate cart from this computer and not from other devices on your network (better security).

To configure such a direct connection, you will need to configure your Ultimate cartridge to something like this: 

::

     *** Ultimate-II Plus 3.3a (112) ***   
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
  



You will also need to configure the ethernet network connection for your modern computer. To connect to the Ultimate cart, you will need to use a different IP-address, but you will need to use the same net mask. E.g. IP-address: 64.64.64.65 and Netmask: 255.255.255.0. Note that in this example you should only change the last number in the IP-address.

Make sure to make a note of the IP-address. You will need this address to reach the Ultimate cartridge on the network.


Using the network connection
----------------------------
At the time of writing there are 4 applications:

1) remote control (using telnet)
2) file transfer (using FTP)
3) using tcp port 64 (raw socket)
4) accessing the network / internet from the C64 (UCI)


Remote control 
--------------
It is possible to completely control the Ultimate cart via a network connection. You will need a telnet application to do so. I will not go into details on how to configure your telnet application. Most standard telnet applications will work out-of-the-box with recent firmware releases. 

Telnet is considered harmful or in other words, not safe. That's why most modern operating systems do not include a telnet binary anymore. You will need to install a telnet client yourself. You can use your favourite package manager. On macOS I use homebrew (https://brew.sh) and simply type 'brew install telnet'. The telnet client is started from the command line. 

Please make sure that your telnet / terminal client supports vt100. The Ultimate remote screen operates at 60 columns by 24 rows. 

To connect to your Ultimate cartrdige simply type on the commandline of your modern computer. 

- telnet <ip-address>

e.g. 

- telnet 192.168.2.64
- telnet 64.64.64.64

If you use windows, make sure to type the ip address in the 'host' input field before making a connection.

Once you're logged in, the screen will look like this:

::

         *** Ultimate-II Plus 3.3a (112) *** Remote ***       
  ────────────────────────────────────────────────────────────
  Usb1    Lexar    microSD RDR                       Ready    
  Usb0    Lexar    USB Flash Drive                   Ready    
  Net0    IP: 192.168.2.64                           Link Up  
  
  
  
  
                                                              
                                                              
  
  
  
  
  
                                                              
                                                              
  
  
  
                                                              
  /                                                  ─F3=Help─





