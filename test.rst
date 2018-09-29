.. warning::

   environment
      A structure where information about all documents under the root is
      saved, and used for cross-referencing.  The environment is pickled
      after the parsing stage, so that successive runs only need to read
      and parse new and changed documents.

   source directory
      The directory which, including its subdirectories, contains all
      source files for one Sphinx project.

.. sidebar:: Sidebar Title
    :subtitle: Optional Sidebar Subtitle

    Subsequent indented lines comprise
    the body of the sidebar, and are
    interpreted as body elements.


=============================================
Firmware Releases for the Ultimate Cartridges
=============================================
This is a list of released firmwares for the 1541 Ultimate, 1541 Ultimate Plus, Ultimate II and Ultimate II+ cartridges by Gideon.

.. contents:: **Firmware releases**
   :depth: 2

Release 3.2a
------------
This is the official 3.2a firmware for the U2+. U2 is not stable yet.

**Download:**

* [3.2a_final.u2p](https://www.facebook.com/groups/1541ultimate/1015560060989775
  3/) (Facebook group)
* [3.2a_final.u2p](Firmware/U2+/3.2a_final.u2p) (local)
* **SHA256:** e4f771934f89da79e68b2d5c4b7f928cecc6db00c6f9432573fca4ada165a8e3

**Changes in this release:**

* Improved DHCP
* SIDFX support in SID player
* FC3 and FC3+ Support improved
* Saving to TAP files repaired
* Many Ultimate 64 related changes

Release 3.2
-----------
**Download:**

* [1541 Ultimate-II / Ultimate-II+ V3.2](http://www.1541ultimate.net/content/download/ultimate_v3.2.zip) (1541ultimate.net)
* [1541 Ultimate-II / Ultimate-II+ V3.2](Firmware/U2/ultimate_v3.2.zip) (local)
* **SHA256:** 3a434d9d7611d2a1282f1e5b87290b33492511323de3026cd24002d782ec8976

**Changes in this release:**

* Completely rewritten SID player, by Wilfred Bos
* Enhanced version of FC3, by Daniël Mantione
* Added Tape Index function, as suggested by Tom Roger Skauen
* Added UCI interface to access the network (TCP/IP and UDP/IP) through Ultimate Command Interface *_(documentation pending)_*
* Many additions and bug fixes by Henning and Markus, including Home Directory, REU load on startup, EasyFlash write support (manual save), and more.
* Some enhancements in FTP server
* Additional bug-fixes.

Release 3.1a
------------
**Download**

**Ultimate-II**

* [1541 Ultimate-II V3.1a](http://www.1541ultimate.net/content/download/ultimate2_495.zip) (1541ultimate.net)
* [1541 Ultimate-II V3.1a](Firmware/ultimate2_495.zip) (local)
* **SHA256:** 6f85347777f7b1adf76fc4f859b0c203c0e5fb0b4d53daf2e1dd05e6e658d2f7

**Ultimate-II+**

* [Ultimate-II+ V3.1a](http://www.1541ultimate.net/content/download/ultimate2plus_495.zip) (1541ultimate.net)
* [Ultimate-II+ V3.1a](Firmware/ultimate2plus_495.zip) (local)
* **SHA256:** 68434f9167813145de32d54758a8397855c3c9bef94501f7fb360a762dfb4f52

**Installation instructions:**

* Copy unzipped file to USB stick
* Put the USB stick in the U2 or U2+

**For the 1541 Ultimate-II:**

Navigate to the unzipped file 'update\_audio\_495.u2u' or 'update\_dual\_drive_495.u2u' and select "Run Update"

**For the Ultimate-II+:**

Navigate to the update_495.u2p file, and select "Run Update".

**Changes in this release:**

* Small bug fixes
* USB fixes:
* No more blocking timeouts, that may hang indefinitely
* Fix for a bug accessing USB2LAN adapters
* U2 audio output fixed; as it was harsh and ugly.


Release 3.1
-----------
**Downloads:**

* [update_v3.1.zip](https://www.facebook.com/groups/1541ultimate/10154585052952753/) (Facebook group)
* [update_v3.1.zip](Firmware/update_v3.1.zip) (local)
* **SHA256:** 0d1d2a1afd78ee5155e69fbb140f3a7634852aeb68bd4cf478956c9ff30b46e4


r474 | gideonz | 2017-03-21 01:11:49 +0100 (di, 21 mrt 2017) | 1 line

**USB fixes:**

* support for sticks that do not reliably reply to the 'inquiry' command
* Byte alignment issue fixed when writing. This caused corrupted G64s to be written sometimes
* Support for composite devices added
* Added support for USB keyboards, to navigate the Ultimate browser menu

**Incorporated patches from Markus & Henning, including, but not limited to:**

* Audio squeal fix, speaker volume addition
* Ultimate DOS V1.1 with added commands
* Added Home Directory support
* Added support for GeoRAM

**IEC fixes:**

* IEC now operates properly on the bus, when it is alone (disabled 1541 drives)
* IEC filename fixes; saving a file to IEC adds the right extension and also removes the extension when loading directory
* IEC should now work with JiffyDOS (not yet supporting the JiffyDOS protocol)
* UltiCopy is working again!

**Other small fixes:**

* Small fix in TCP support (TCP hangup on retransmission)
* Save disk twice bug fixed
* Fixed load errors on tape adapter cable with some USB 3.0 cables
* Keyboard "racekeys" fixed
* Reduced Link Up time for the Ethernet port
* Ultimax mode ROMs now allow video data in ROM

## Release 3.0e
**Downloads:**

* [Preinstalled 3.0e](firmware/3.0e_452.u2p) (local)
* **SHA256:**

*No release notes available*

Release 3.0c
------------
**Downloads:**

* [3.0c_424.u2p](https://www.facebook.com/groups/1541ultimate/10154074122137753/) (Facbook group)
* [3.0c_424.u2p](Firmware/3.0c_424.u2p) (local)
* **SHA256:** ec6b496a3988f57391f7798a7575cc435059309c37ebbda09ba05a317407b970

**Ultimate-II+ fixes: 3.0c rev 423**

* Fixed speaker disable
* Fixed G64 loading
* Fixed IEC for use with JiffyDOS and single byte fetches
* Increased output volume on codec output
* Auto audio / REU select for MOD player (yet to do for SID player)


Release 3.0 beta 7
------------------
**Downloads:**

* [1541 Ultimate-II V3.0 beta 7 - audio version, single drive](http://www.1541ultimate.net/content/download/1541u2_3.0beta7.zip) (1541ultimate.net)
* [1541 Ultimate-II V3.0 beta 7 - audio version, single drive](Firmware/1541u2_3.0beta7.zip) (local)
* **SHA256:** 35e53bcf942a9e3b06a5a532d3d6bbf60938e75cb177619e912266b1d2107c28

**Installation instructions:**

* In order to update from 2.x: place the update.bin into the root of your SD card.
* If you already have 3.x installed, select the update.u2u file from the browser menu. You can have the updater either on SD card or on a USB device.
* If you want to go back to 2.6; run the 'revert.u2u' file from the browser menu.

**Changes in this release:**

**r297 | gideonz | 2016-04-15 21:27:25 +0200 (Fri, 15 Apr 2016)**

* Prepared for release 3.0b7
* Processor flag error fixed.
* Some 6502 opcode testing done. Fixed ADC in decimal mode.

**Some fixes:**

* ISSUE 189: Mount disk is now performed when C64/drive is not frozen
* ISSUE 191: Loading a file from within T64 (and D64) could fail at times due to special chars. Fixed
* ISSUE 193: Tape grab to TAP file fixed (at least that the option to run it will work)
* ISSUE 204: TCP slowdown fixed; bug in USB driver
* ISSUE 207: Typo fixed that caused "Save to disk" to fail with a 0 byte file
* OTHER: SID file with faulty header now no longer causes Flash corruption
* OTHER: Tape play / record functions updated

**r276 | soci | 2016-01-17 07:35:38 +0100 (Sun, 17 Jan 2016)**

* Fix wrong DDRA readback (typo)
* The TASM-RR cartridge is not REU compatible
* Fix for PB6/7 keyboard freeze bug


Release 3.0 beta 5
------------------
**Download:**

* [1541 Ultimate-II V3.0 beta 5](http://www.1541ultimate.net/content/download/1541u2_3.0beta5.zip) (1541ultimate.net)
* [1541 Ultimate-II V3.0 beta 5](Firmware/1541u2_3.0beta5.zip) (local)
* **SHA256:** f4100a4f4f3353fb0e24f6b14d15155c4ddc8d5a6abfcf59c9339c537407e946

**Installation instructions:**

* In order to update from 2.x: place the update.bin into the root of your SD card.
* If you already have 3.x installed, select the update.u2u file from the browser menu. You can have the updater either on SD card or on a USB device.
* If you want to go back to 2.6; run the 'revert.u2u' file from the browser menu.

**Changes in this release:**

**Major:**

* BUGFIX: Processor's Data Cache stored result of IO read, causing wrong values to be read from the cache

**Minor:**

* C64 Keyboard scan made a bit slower  (not tested)
* Fixed configuration drop down
* Fixed clock settingsa
* Mount disk made first option in D64 file type
* Updated Final 3 cart.


Release 3.0b4
-------------
**Download:**

* [1541 Ultimate-II 3.0 beta 4](https://www.facebook.com/groups/1541ultimate/10153275033302753/) (Facbook group)
* [1541 Ultimate-II 3.0 beta 4](Firmware/1541u2_3.0beta4.zip) (local)
* **SHA256:** 4ac8fad3ab2ad608b7e159c9ddfbf3dd4f31a2dbda8af8a58e781d75cbdb6ee8

**Changes in this release:**

* The FPGA platform has gotten an upgrade. There is now a faster RISC processor
  on board (~10 times faster), and I have re-written the USB host controller,
  which has become ~50 times faster. The external memory of the FPGA also runs
  faster, and delivers now also approx. 7 times more bandwidth. With this
  faster platform, it has become possible to run a multithreaded OS.
* There is now support for USB2LAN adapters, and 3.0beta4 runs two services: a
  (raw-)telnet (VT100) server that brings up the menu, and an FTP daemon for
  basic file transfer.
* There is now support for reading the directories of D71 and D81 files in the
  browser.
* There is a 'CD' command in the software IEC, and other improvements have been
  made to the soft IEC driver.
* There is now a copy command in the file browser, that works with C=C/C=V (or
  CTRL-C / CTRL-V). It is not that fast, but for small files it works. You can
  also copy files from inside a D64/T64 to another location in the file system.
  The other way around is still under development, but will soon be possible as
  well.

*UltiCopy is disabled for now, because it still needs to be ported to the
multi-threaded operating system.*


Release notes 2.6k
------------------
**Downloads:**

**Audio, single drive**

* [1541 Ultimate-II V2.6k (audio, single
  drive)](http://www.1541ultimate.net/content/download/1541u2_2.6k_audio.zip)
  (1541ultimate.net)
* [1541 Ultimate-II V2.6k (audio, single drive)](Firmware1541u2_2.6k_audio.zip)
  (local)
* **SHA256:** 9ce89fe1cef9446134c9df5a104f3e1413cb598cea18000ccdc0e065833b5874

**Dual drive, no audio**

* [1541 Ultimate-II V2.6k (dual drive)](Firmware/1541u2_2.6k_dual_drive.zip)
  (1541ultimate.net)
* [1541 Ultimate-II V2.6k (dual drive)](Firmware/1541u2_2.6k_dual_drive.zip)
  (local)
* **SHA256:** 1868867868992a6367d59eb9cb2e75c50cfd5af5a0490b3b8642c66b007300af

**Changes in this release:**

* Support new Flash chip, in order to support board revision D.
* Removed non-functional double entry of USB module in configuration screen.

==*If you like to switch between audio and dual drive version, please make sure that you select "Force All" in the updater, otherwise the FPGA image won't be replaced and nothing will change.*==


Release notes 2.6h
------------------
**Downloads**

* [1541u2_2.6h.zip](http://www.1541ultimate.net/content/download/1541u2_2.6h.zip) (1541ultimate.net)
* [1541u2_2.6h.zip](Firmware/1541u2_2.6h.zip) (local)

**Changes in this release:**

| Version 2.6h contains some small fixes on top of 2.6d.
| This build is a DUAL DRIVE version with NO SID emulation.

* Timing fixed for C64C
* Newer version of built-in MOD player
* Bug fixes regarding USB stick removal
* Enhancements under the hood for networking support. Network support will be
  enabled later, is not part of this version!


1541U-II Update 2.6d
--------------------
**Download:**

* [1541 Ultimate-II V2.6d](http://www.1541ultimate.net/content/download/1541u2_2.6d.zip) (1541ultimate.net)
* [1541 Ultimate-II V2.6d](Firmware/1541u2_2.6d.zip) (local)
* **SHA256:** 769674d334d0f6dea3893d61d1a0028f31cc7a2ee9a3ff028bb13ca8976637b2

Version 2.6d contains some small fixes on top of 2.6c.

**Release notes 2.6d:**

* Ultimax mode forced now correctly implemented (solves issue with freeze and DMA load)* Programmable cartrige emulation timing* Some drive emulation enhancements
* FIXED: Ultimax mode forced now correctly implemented (solves issue with freeze and DMA load)
* FIXED: Updater now works on C128... (not all C128 issues are fixed)
* ADDED: Programmable cartrige emulation timing
* IMPROVED: Some drive emulation enhancements

**Release notes 2.6c:**

* This version does include SID, but is just single-drive. It does include the Ultimate Audio module. Different builds may become available upon request.
* FIXED: USB stick present on boot time caused the Ultimate-II to crash when loading a file from SD at initialisation time (kernal rom / drive rom)
* FIXED: Starting a program with RUN sometimes caused the ultimate to become unresponsive when freezing afterwards.
* FIXED: Now reads USB sticks with FAT16 format, but without partition table.
* See for additional information the release notes of firmware V2.6


1541U-II Update 2.6
-------------------
**Download:**

* [1541 Ultimate-II V2.6](http://www.1541ultimate.net/content/download/1541u2_2.6.zip) (1541ultimate.net)
* [1541 Ultimate-II V2.6](Firmware/1541u2_2.6.zip) (local)
* **SHA256:** 2bd8f9ce9936d98ca61174fbf0463b7066b68532126586a41d5925e3b811ffb0

**Version 2.6 includes some new features:**

* Disk Copier from real drives to .D64 images
* Command Interface
* Ultimate-II DOS V1.0 (command target)
* Kernal replacement function

**... and some important fixes, including:**

* TAP file recorder failed miserably on high latency write devices. Rewritten; should work better now.
* Drive data timing has improved. Timing is now dependent on the data track itself, not on the speed setting of the VIA. This fixes some protected titles in G64 format.

**Release information:**

* This version does *not* include SID, but it does include the Ultimate Audio module. Different builds may become available upon request.
* The internal copier is still in beta. It has been tested with some of my drives, but there might be drives out there that won't work. Make sure you have an IEC link from the Ultimate to a real drive to use this function. (No need to have a link to the computer.) There is still no retry mechanism; sectors that failed to read correctly will not be re-read.
* The Kernal replacement function is critical when it comes to timing. Tested on two machines only. Might not work on C128.

**Installation instructions:**

* Unzip the downloaded file into the root of your SD card.
* Place the SD card in the 1541Ultimate II.
* Boot your Commodore machine
* Wait for instructions and remove SD after flashing. Suggestion: remove 'update.bin' from the root of the SD, using the PC or the delete command in the Ultimate.

***Command Interface and Ultimate-II DOS***

See the [documentation](Documentation/command_interface_v1.0.pdf) of the Command Interface module for knowing how to use it!

See the [documentation](Documentation/ultimate_dos_v1.0.pdf) of the Ultimate-II DOS, to get to know what you can do with the Command Interface in this firmware release.


1541U-II Update 2.5 and 2.5+
----------------------------
**Download:**

* [1541 Ultimate-II V2.5](http://www.1541ultimate.net/content/download/1541u2_2.5.zip) (1541ultimate.net)
* [1541 Ultimate-II V2.5](Firmware/1541u2_2.5.zip) (local)
* **SHA256:** 94d6590a882c64a01ec74db52510554d9d6aadc901b405e69f685c534c295b40

**Version 2.5 includes some new features:**

* File viewer
* Selectable colors in user interface

Version **2.5** also includes some fixes for nasty memory allocation bugs that existed when using USB sticks. Removal of a USB device is now at least a lot safer. :-) Also, some file system bugs were fixed.

**Installation instructions:**

* Unzip the downloaded file into the root of your SD card.
* Place the SD card in the 1541Ultimate II.
* Boot your Commodore machine
* Wait for instructions and remove SD after flashing. Suggestion: remove 'update.bin' from the root of the SD, using the PC or the delete command in the Ultimate.

_***Ultimate Audio module***_

There is also a special version of 2.5; including a special 7-voice audio engine. This version, based on the same 2.5 with the bugfixes can be downloaded here:

* [1541 Ultimate-II V2.5+](http://www.1541ultimate.net/content/download/1541u2_2.5_uaud.zip) (1541ultimate.net)
* [1541 Ultimate-II V2.5+](Firmware/1541u2_2.5_uaud.zip) (local)
* **SHA256:** c19d9ad9c81ac79238ca06aedc2f62922e88b72541bb6cbfbd29d1233ebdf7ca

See the [documentation](Documentation/ultimate_audio_v0.2.pdf) of the Ultimate
Audio module for knowing how to use it!

**Version 2.5+ is a special FPGA build; it only supports ONE floppy drive, in
favor of extra audio functionality.**


Release 2.4a / 2.4c 1541U1/II Update
------------------------------------
**Downloads:**

**1541 Ultimate-I (Plus)**

* `1541 Ultimate-I (Plus) V2.4a
  <http://www.1541ultimate.net/content/download/1541u1_2.4a.zip>`_
  (1541ultimate.net)
* **SHA256:** 88051bc7380f181b30d69da5405e481d574238aa9e246e473e11ebc34e7d5c75

**1541 Ultimate-II**

* `1541 Ultimate-II V2.4c
  <http://www.1541ultimate.net/content/download/1541u2_2.4c.zip>`_
  (1541ultimate.net)
* **SHA256:** 2682f90cd7ba650a9a50af5260f3e99cc523eecd7a456e060239cf82764c0a1b

**Installation instructions:**

**For 1541U-I:**

* Unzip the downloaded file into the root of your SD card.
* Place the SD card in the 1541Ultimate I/II.
* Boot your Commodore machine

**For 1541U-II:**

* Wait for instructions and remove SD after flashing. <br> Suggestion: remove
  'update.bin' from the root of the SD, using the PC or the delete command in
  the Ultimate.

**Version 2.4c includes the fixes that TLR made to the firmware, and adds the following features:**

* CRT load (just by selecting the file, not on boot time);
* EasyFlash support (reading only, writing is not yet implemented and is under
  discussion);
* Flashing and running custom FPGAs (Ultimate-II only), especially for those
  who want to do FPGA development without JTAG cable. FPGA bitfile will be
  flashed into the spare area of the Flash memory device, and the FPGA is
  booted from there. So there is no risk of bricking your device. (Flashing
  needs to be done for every boot still, optimizations will follow.)
* For the rest, a lot of work has been done 'under the hood'; especially in
  preparation of a native command interface to control the Ultimate from I/O
  space. But since this is not yet ready, it's not included (=not enabled) in
  the 2.4 firmware.

.. note:: 2.4a and 2.4c are the same, except for the update program
          itself.

Release 2.3 - 1541 Ultimate, 1541 Ultimate+ and 1541 Ultimate-II
----------------------------------------------------------------
**Download:**

* `1541 Ultimate-I (Plus)
  <http://www.1541ultimate.net/content/download/1541u1_2.3.zip>`_
  (1541ultimate.net)
* **SHA256** bc09cb97a970f038893e26f585bdb747f423bd2e5bbeecf22071388d642cd3cb

* `1541U-II Firmware V2.3
  <http://www.1541ultimate.net/content/download/1541u2_2.3.zip>`_
  (1541ultimate.net)

* **SHA256:**

**Installation instructions:**

1. Make sure that in your current configuration, the "application to boot" is
   set to "appl.bin" (the default).
2. Unzip the zip file into the ROOT of an SD-card, of which you have made sure
   that the 1541 Ultimate can read it.
3. Place the SD-card in the 1541U, and make sure the 1541U is correctly
   inserted in a C64/C128 expansion slot.
4. Turn on the C-64 and watch the screen output.
5. Turn off the C-64 when the update is finished.

**Installation instructions**

1. Unpack this file into the root of your micro SD.
2. Place the SD-card in the 1541U-II, and make sure the 1541U is correctly
   inserted in a C64/C128 expansion slot.
3. Turn on the C-64 and watch the screen output.
4. Turn off the C-64 when the update is finished and remove the SD
5. Delete the update.bin file from the SD.

**Changes in this release**

* REU fixed.
* Timing module for cartridge slot simplified to make things work on an SX-64.
* D64 listing corrected for some non-conformant files.
* Most audio options disabled for Ultimate-I.
* A lot of small things modified under the hood (not yet visible as feature for
  the user.)
* Some testing done on both Ultimate-I as well as Ultimate-II.


1541U Firmware V1.7 beta
------------------------
**Download:**

* `1541 Ultimate V1.7
  beta <http://www.1541ultimate.net/content/download/1541u_v1.7beta.zip>`_
  (1541ultimate.net)
* **SHA256:** 95ae3f25bf795f9a7a04e12b3ca1164bf83e2347cafc23af4d35d6c7c81187d1

**Installation instructions:**

1. Make sure that in your current configuration, the "application to boot" is
   set to "appl.bin" (the default).
2. Unzip the zip file into the ROOT of an SD-card, of which you have made sure
   that the 1541 Ultimate can read it.
3. Place the SD-card in the 1541U, and make sure the 1541U is correctly
   inserted in a C64/C128 expansion slot.
4. Turn on the C-64 and watch the screen output.
5. Turn off the C-64 when the update is finished.

**In comparison to 1.6, the following has been changed:**

* The freezer has been made more robust. (Needs more testing)
* Minor fixes in the IEC interface (but not yet satisfactory)
* SID player has been added
* Epyx Fastloader cartridge has been added
* Support for custom carts has been added (8K/16K, as well as existing carts)
* Support for (custom) Ocean and System3 cartridges added.

.. note:: **This is a BETA release.**

