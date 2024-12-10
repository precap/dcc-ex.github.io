.. include:: /include/include.rst
.. include:: /include/include-l1.rst
.. include:: /include/include-ex-cs.rst
  
|EX-CS-LOGO| |donate-button|

.. index:: EXCSB1, EX-CSB1

**********************************
EX-CSB1 Quick Setup Guide
**********************************

This quick startup guide is designed to have you configured and setup to run trains in 5 minutes. After all, the point is to enjoy running trains, not sifting through more information than you need until you are ready. These in structions are for DCC locomotives. For more detailed information, or to configure for running DC trains, see the :doc:`EX-CSB1 Operating Manual <manual>`

What You Will need
=====================

* An EX-CSB1 Command Station
* A Power supply (12V - 16V DC see :ref:`Power Supplies <reference/hardware/power-supplies:power supplies>`)
* A DCC loco (DC can work also)
* Track
* A throttle (You can use your phone or a computer - see below)
* 16 to 28AWG/1.5mm^2 Wire, preferably in 2 colors with 1/8"/6mm insulation stripped (and wire tinned if stranded)
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

.. note::

   Start with all power disconnected!! Before connecting any wires to your command station or tracks, make sure you have unplugged the power supply from the wall or removed the barrel connector from the command station. It is crucial to ensure that the command station has no power while you are working on your connections.

Summary or Super-Quick Start
============================

In summary, you need just two basic wiring connections to the EX-CSB1 to be up and running trains:

* Track connected to Track A Output
* Power supply input connected to Power IN DC barrel jack

And to connect via WiFi to the EX-CSB1 you need a wireless smart device running either:

* Engine Driver or EX-ToolBox for Android
* WiThrottle for Apple iOS

Connecting to the EX-CSB1 via WiFi:

* Select the WiFi network named DCCEX_xxxxxx, and use the corresponding password PASS_xxxxxx (where xxxxxx is identical in each case) shown on your EX-CSB1's OLED display
* Tell your smart device not to worry about there being no Internet connection
* Launch throttle app, which should connect automatically

Track Connection
-----------------

There are 2 track output power connectors marked A and B. In the standard DCC-EX configuration of a CSB1, A is configured for DCC MAIN operation, and B is configured for PROG or programming track output. We recommend connecting your track to the A MAIN output initially to test your Command Station. To alter this default configuration of DCC outputs, or for DC Mode, you would need to configure outputs with a TrackManager command in the mySetup.h file or via Routes. See :doc:`the TrackManager page </trackmanager/index>`

.. figure:: /_static/images/ex-csb1/ab_outputs.png
   :alt: Track A and B Outputs
   :scale: 90%
   :align: center

   Track A and B Outputs

The pluggable male screw terminals accept to 16 to 28 AWG/1.5mm^2 gauge solid or stranded wire. If you use stranded, we recommend "tinning" the ends of the wire to make a good connection and ensure that stray wire whiskers don't stray outside the screw terminals and cause a short circuit. Larger wire can handle more current and provide less resistance.  18-22 AWG is a good start. Keep your wires short by mounting the CS close to the track. See XXX for more information or wire gauge.

Using a small flat-bladed screwdriver, loosen both screws on the MAIN (A) Track Output being careful not to screw them all the way out. The screws just need to be loosened enough to fit your wires into the holes. Tighten down both screws once you have inserted the wires making sure to not overtighten. You can pull the connector out of its socket to remove it from the |EX-CSB1| to make this easier. Remember push the connector all the way into the connector on the board to snap it back in place.

.. figure:: /_static/images/ex-csb1/csb1_insert_wire3.png
   :alt: Inserting Track Wires
   :scale: 40%
   :align: center

   Inserting wires

.. figure:: /_static/images/ex-csb1/csb1_insert_wire4.png
   :alt: Tightening Screws
   :scale: 40%
   :align: center
   
   Tightening Screws


.. figure:: /_static/images/ex-csb1/csb1_insert_wire.png
   :alt: Unplugging connector to insert wires
   :scale: 40%
   :align: center

   Optionally unplugging connector to insert wires

.. figure:: /_static/images/ex-csb1/csb1_insert_wire2.png
   :alt: Wires properly inserted
   :scale: 40%
   :align: center
   
   Wires properly inserted and plug inserted



.. NOTE:: The power connection to your track will be either wires you solder yourself to the rails or via a power connector that plugs into track (such as Kato Unitrack). We will leave it up to you to determine the proper connection to your track. 

Connect the other ends of the track output wires to your track. While not critical at this stage when using DCC, it is best to keep to a standard where the RED wire is connected to the outside rail of the track to make things easier when using feeders to track sections or adding reversing loops. XXX need to mention DC here with a link?

[insert image - connecting wires to track]


USB Connection
------------------

Connect the USB-C end of the USB cable to the |EX-CS|. Connect the other end to your computer or laptop on which you will run |EX-WT|.

.. figure:: /_static/images/ex-csb1/csb1_power_usb.png
   :alt: Connecting USB cable
   :scale: 40%
   :align: center
   
   Connecting USB cable

Note that 5V power is supplied with the USB connection, so the single green 3.3V LED illuminates (See figure). This powers the electronics on the board for basic testing and to apply software updates, but will not power the track outputs until power is applied through the barrel jack. You do NOT need USB power for normal operation. The blue WiFi LED will also illuminate indicating the CSB1 is setup for a WiFi connection. More on wifi here XXX. And last, the display will show status information. More on this below XXX

Power Connection
------------------

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

To fully power the CSB1, just plug your power supply into the mains power (aka wall outlet) and connect the barrel end to the Command Station. Make sure your power supply matches the needs of your setup: the voltage should be between 12V and 25V DC, depending on the scale of your locomotives, and it should provide at least 2A of current with good over-current performance and voltage stability. To get the most out of your EX-CSB1, we suggest using a modern switching power supply with 4A or more. For Z scale, 12V is usually enough, but for N, HO, and OO scales, we recommend using between 14V and 16V DC. It’s important that your DC power is well-regulated which is why we suggest a modern switch-mode power supply with double insulation and strong overload protection.

.. figure:: /_static/images/ex-csb1/csb1_barrel_insert.png
   :alt: Inserting barrel plug
   :scale: 40%
   :align: center

   Inserting Power Supply Barrel Plug

When you connect power to the CSB1, you should see one or both bright green power LEDs light up (5V and 3.3V power), confirming that the electronics are working. However, for safety, track output power will be off by default when you first plug in the EX-CSB1. This is to prevent power from accidentally being applied to your layout before everything is ready. If you prefer, you can change this default setting [link] XXX.

.. figure:: /_static/images/ex-csb1/csb1_power_barrel.png
   :alt: Barrel Power LEDs
   :scale: 40%
   :align: center

   Barrel Plug Power LEDs

You should see status information on the display including the CSB1 firmware version, track power status, free memory, and WiFi connection information. If you do not have a display, you will need to connect a serial monitor XXX [insert link]

.. figure:: /_static/images/ex-csb1/csb1_oled.png
   :alt: OLED Status Display
   :scale: 40%
   :align: center

   OLED Status Display

The DCC-EX EX-CSB1 Command Station/Booster will power up in WiFi Access Point mode as configured out of the box, with a Wifi network SSID of DCCEX_xxxxxx and password of PASS_xxxxxx (where xxxxxx is the last 6 digits of the MAC address of the CSB1), both of which will be visible on the OLED display (or serial monitor log XXX [insert link]) after it boots so you can connect with a phone throttle. This quick start covers initial testing with USB connection to a computer, see XXX for connecting via WiFi [insert link]

Access Point (AP) mode creates a separate WiFi network on the Command Station itself, whereas Station (STA) mode allows the Command Station to join as a WiFi device on your home or layout WiFi network. We have the EX-CSB1 set to default to AP mode for convenience of being able to get up and running quickly.

The WiFi LED will illuminate once WiFi is configured and ready as an Access Point (or Station if reconfigured for STA mode.)

[insert link] XXX figure link showing WiFi LED


Connect EX-WebThrottle
-----------------------

You can connect to the EX-CSB1 using both an app via Wifi on a smartphone or tablet, and on a PC using WebThrottle with the PC plugged into the EX-CSB1's USB-C port. Detailed instructions are here https://dcc-ex.com/ex-commandstation/controllers.html#choosing-a-throttle-controller. As mentioned above, in this quick start we will be using EX-Webthrottle.

Begin by running |EX-WT| by clicking this link. XXX [insert link] Detailed instructions on how to use WebThrottle is here XXX. 
How detailed to get here? We don't want to just repeat everything from the WT page, but also don't want to make a user jump back and forth between pages XXX.

XXX images of running webthrottle

Confirm startup
----------------

[insert link] Show and explain the startup screen

Turn On Track Power
--------------------

Show how to slide the power slider, etc

Run a locomotive
------------------

reverse this and power? when to put loco on track? XXX

DCC Operation
---------------

The EX-CSB1 is set to operate in DCC mode by default. If you want to switch to any of the outputs to DC mode, you can find instructions on how to do that here :doc:`TrackManager page </trackmanager/index>`

Booster Mode
--------------

The |EX-CSB1| as the name implies can operate as a Command Station or a Booster. See [insert link] for instructions on how to use the EX-CSB1 as a booster.

Full EX-CSB1 Operating Manual
------------------------------

[insert link]
