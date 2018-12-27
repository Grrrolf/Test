| this is |reg| and this is an |left arrow| and an |arrow up|
| what you see here |left arrow| is a left arrow.

============ ===========
key          description
============ ===========
|left arrow| smile
============ ===========

============ ===========
key          description
============ ===========
|left arrow| |smile|
============ ===========


.. warning::

   environment
      A structure where information about all documents under the root is
      saved, and used for cross-referencing.  The environment is pickled
      after the parsing stage, so that successive runs only need to read
      and parse new and changed documents.

   source directory
      The directory which, including its subdirectories, contains all
      source files for one Sphinx project.

+--------------------+----------+-----------------------------------+
| Header 1           | Header 2 | Header 3                          |
+====================+==========+===================================+
| | Item 1           |          | | This is another test with a long|
| | \ |arrow up|     |          | | line that does not wrap automat-|
| | \ |left arrow|   |          | | ically. Manually works?         |
+--------------------+----------+-----------------------------------+

.. table:: **Test table for autowrap**
   :widths: auto
   :align: left

   ============   =====
   row1           row 2
   ============   =====
   |left arrow|   Truth is somethign intersting don't you think so? But will it also wrap or not! I hope it does, but don't think it will. But it seems that it actuall does wrap? What's going on here!
   |left arrow|   False
   ============   =====

.. sidebar:: Sidebar Title
    :subtitle: Optional Sidebar Subtitle

    Subsequent indented lines comprise
    the body of the sidebar, and are
    interpreted as body elements.

+--------------+---+-----------+
|  simple text | 2 | 3         |
+--------------+---+-----------+
|  simple text | 2 | 3         |
+--------------+---+-----------+
|  simple text | 2 | 3         |
+--------------+---+-----------+
|  simple text | 2 | 3         |
+--------------+---+-----------+
|  simple text | 2 | 3         |
+--------------+---+-----------+
|  simple text | 2 | 3         |
+--------------+---+-----------+


============ ===========
key          description
============ ===========
|left arrow| |smile|
============ ===========

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
  
And another screen:
::
         *** Ultimate-II Plus 3.3a (112) *** Remote ***       
  ────────────────────────────────────────────────────────────
  Usb1    Lexar    microSD RDR                       Ready      
  Usb0    Lexar    USB Flash Drive                   Ready    
  Net0    IP: 192.168.2.64                           Link Up  
  
  
  
  
  
                                                              
  
  
  
   
  
  
                                                            
  
  
  
  
                                                            
  /                                                  ─F3=Help─


.. role:: red
.. |left arrow| unicode:: U+2B05 U+FE0E .. LEFTWARDS BLACK ARROW
.. |arrow up|   unicode:: U+2B06 U+FE0E  .. UPWARDS BLACK ARROW
.. |smile|      unicode:: U+1F603       .. grinning face with open mouth
.. |reg|        unicode:: U+000AE       .. REGISTERED SIGN


