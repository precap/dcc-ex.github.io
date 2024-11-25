.. include:: /include/include.rst
.. include:: /include/include-l1.rst
.. include:: /include/include-ex-cs.rst
  
|EX-CS-LOGO| |donate-button|

.. index:: EXCSB1, EX-CSB1

**********************************
EX-CSB1 Quick Setup Guide
**********************************

This quick startup guide is designed to have you configured and setup to run trains in 10 minutes. After all, the point is to enjoy running trains, not sifting through more information than you need until you are ready. These in structions are for DCC locomotives. For more detailed information, or to find out how to run DC trains, see the :doc:`EX-CSB1 Operating Manual <manual>`

What You Will need
=====================

* An EX-CSB1 Command Station
* A Power supply (12V - 16V DC see :ref:`Power Supplies <reference/hardware/power-supplies:power supplies>`)
* A DCC loco (DC can work also)
* Track
* A throttle (You can use your phone or a computer - see below)
* 16 to 28AWG/1.5mm^2 Wire, preferably bi-colored with 1/8"/6mm insulation stripped (and wire tinned if stranded)
* Jeweller's flat bladed screwdriver (1.5 - 2mm blade)
* A laptop or other computer* with an internet connection and chromium based browser (Chrome, Edge,etc.)
* A USB cable with one end a USB-C for the EX-CSB1, and the other to suit your PC*

 \*Optional for connecting connecting to a computer for WebThrottle, JMRI and to update/add EXRAIL Scripts to the |EX-CS|

Board Layout
==============

.. figure:: /_static/images/ex-csb1/csb1_render_layout_top.png
   :alt: DCC-EX EX-CSB1 Express
   :scale: 42%

   EX-CSB1 top (click image to enlarge it)


Connections
=====================

Start with all power disconnected
----------------------------------

Before connecting any wires to your command station or tracks, make sure you have unplugged the power supply from the wall or removed the barrel connector from the command station. It is crucial to ensure that the command station has no power while you are working on your connections.

.. image:: /_static/images/ex-csb1/pluggable_connectors.png
   :alt: Pluggable Track Output Connectors
   :scale: 40%
   :align: right

Track Connection
-----------------

There are 2 track output power connectors marked A and B. A is usually the MAIN track while B is for Programming locos. In the standard DCC-EX configuration of a CSB1, A is configured for DCC MAIN operation, and B is configured for PROG or programming track output. We recommend connecting your track to the A MAIN output initially to test your Command Station. To alter this default configuration of DCC outputs, or for DC Mode, you would need to configure outputs with a TrackManager command in the mySetup.h file or via Routes. See :doc:`the TrackManager page </trackmanager/index>`

The pluggable male screw terminals accept to 16 to 28 AWG/1.5mm^2 gauge solid or stranded wire. If you use stranded, we recommend "tinning" the ends of the wire to make a good connection and ensure that stray wire whiskers don't stray outside the screw terminals and cause a short circuit. Larger wire can handle more current and provide less resistance.  18-22 AWG is a good start. Keep your wires short by mounting the CS close to the track. See XXX for more information or wire gauge.

[plug image]

Using a small flat-bladed screwdriver, loosen both screws on the MAIN (A) Track Output being careful not to screw them all the way out. The screws just need to be loosened enough to fit your wires into the holes. Tighten down both screws once you have inserted the wires. You can pull the connector out of its socket to remove it from the |EX-CSB1| to make this easier. Remember to snap it back in place when finished.

[insert image]

Insert the track wires into each screw terminal and tighten them down so they grip firmly while not so tight as to break the connector.

[insert image]

.. NOTE:: The power connection to your track will be either wires you solder yourself to the rails or via a power connector that plugs into track (such as Kato Unitrack). We will leave it up to you to determine the proper connection to your track. 

Connect the other ends of the track output wires to your track. While not critical at this stage when using DCC, it is best to keep to a standard where the RED wire is connected to the outside rail of the track to make things easier when using feeders to track sections or adding reversing loops. XXX need to mention DC here with a link?

[insert image]


USB Connection
------------------

Connect the USB-C end of the USB cable to the |EX-CS|. Connect the other end to your computer or laptop on which you will run |EX-WT|.

[insert image]

Power Connection
------------------

.. image:: /_static/images/ex-csb1/barrel_jack1.png
   :alt: Barrel Jack
   :scale: 40%
   :align: right

The CSB1 has a 2.1mm x 5.5mm power jack. If you already have a power supply with bare wires, you can use an optional 2.1mm x 5.5mm screw terminal block adapter. For N and HO scale you would normally use a 12V to 15V DC power supply, but be sure to check the manual for your loco/decoder combination for the correct voltage. For more information about power supplies, including how to use one power supply to supply all the different voltages on your layout, see :ref:`Power Supplies <reference/hardware/power-supplies:power supplies>`. 

.. figure:: /_static/images/power/2_1mm_screw_terminal_adapter.png
   :scale: 40%
   :align: left
   :alt: 2.1mm screw terminal adapter

   2.1mm Screw Terminal Adapter

.. figure:: /_static/images/12v-3A-brick.jpg
   :alt: 12V 3A brick power supply
   :scale: 100%
   :align: center

   12V/3A Power Supply


|force-break|

Testing Your Command Station
============================================

Connect Track Input Power
--------------------------

To power up the CSB1, just plug your power supply into the mains power (aka wall outlet) and connect the barrel end to the Command Station. Make sure your power supply matches the needs of your setup: the voltage should be between 12V and 25V DC, depending on the scale of your locomotives, and it should provide at least 2A of current with good over-current performance and voltage stability. To get the most out of your EX-CSB1, we suggest using a modern switching power supply with 4A or more. For Z scale, 12V is usually enough, but for N, HO, and OO scales, we recommend using between 14V and 16V DC. It’s important that your DC power is well-regulated which is why we suggest a modern switch-mode power supply with double insulation and strong overload protection.

When you connect power to the CSB1, you should see one or both bright green power LEDs light up, confirming that the electronics are working. However, for safety, track output power will be off by default when you first plug in the EX-CSB1. This is to prevent power from accidentally being applied to your layout before everything is ready. If you prefer, you can change this default setting [link] XXX.

You should see status information on the display including the CSB1 firmware version. (If you do not have a display, you will need to connect a serial monitor XXX This is a mess of having to have so many options and send people back and forth and have an entire section on using a serial monitor. Just link to it? Yeah... link to it... it's why I insisted on an OLED display XXX PMA :-P )

The DCC-EX EX-CSB1 Command Station/Booster will power up in WiFi Access Point mode as configured out of the box, with a Wifi network SSID of DCCEX_xxxxxx and password of PASS_xxxxxx, both of which will be visible on the OLED display (or serial monitor log) after it boots.

XXX figure link to OLED display. Also link to serial monitor log section?

Access Point (AP) mode creates a separate WiFi network on the Command Station itself, whereas Station (STA) mode allows the Command Station to join as a WiFi device on your home or layout WiFi network. We have the EX-CSB1 set to default to AP mode for convenience of being able to get up and running quickly.

The WiFi LED will illuminate once WiFi is configured and ready as an Access Point (or Station if reconfigured for STA mode.)

XXX figure link showing WiFi LED


Connect EX-WebThrottle
-----------------------

You can connect to the EX-CSB1 using both an app via Wifi on a smartphone or tablet, and on a PC using WebThrottle with the PC plugged into the EX-CSB1's USB-C port. Detailed instructions are here https://dcc-ex.com/ex-commandstation/controllers.html#choosing-a-throttle-controller. For this quick start, we will be using EX-Webthrottle.

Run |EX-WT| by clicking this link. [insert link] Detailed instructions on how to use WebThrottle is here XXX. 
How detailed to get here? We don't want to just repeat everything from the WT page, but also don't want to make a user jump back and forth between pages.

XXX images of running webthrottle

Confirm startup
----------------

Again, have to show how to use the log here. How can we do a condensed version? XXX

Turn On Track Power
--------------------

Run a locomotive
------------------

reverse this and power? when to put loco on track? XXX

DCC Operation
---------------

The EX-CSB1 is set to operate in DCC mode by default. If you want to switch to any of the outputs to DC mode, you can find instructions on how to do that here :doc:`TrackManager page </trackmanager/index>`
