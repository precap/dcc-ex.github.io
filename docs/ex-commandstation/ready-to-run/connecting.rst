.. include:: /include/include.rst
.. include:: /include/include-l1.rst
.. include:: /include/include-ex-csb1.rst
  
|EX-CS-LOGO| |donate-button|

.. index:: EXCSB1, EX-CSB1

|EX-CSB1|

**********************************
EX-CSB1 Quick Setup Guide
**********************************

|conductor| |tinkerer| |engineer| |support-button|

This quick startup guide is designed to have you configured and setup to run trains in 5 minutes. After all, the point is to enjoy running trains, not sifting through more information than you need until you are ready. These instructions are for DCC locomotives. For more detailed information, to configure for running DC trains, or to use different throttles like EX-WebThrottle or JMRI, see the :doc:`EX-CSB1 Operating Manual <manual>`

What You Will need
=====================

* An |EX-CSB1|
* A Power supply (12V - 16V DC see :ref:`Power Supplies <reference/hardware/power-supplies:power supplies>`)
* A DCC loco (If you are here to run DC, please go to todo XXX)
* Track
* 16 to 28AWG/1.5mm^2 Wire, preferably in 2 colours with 1/8"/6mm insulation stripped (and wire tinned if stranded)
* Jeweller's flat bladed screwdriver (1.5 - 2mm blade)
* A WiFi capable smart device like a phone or tablet to control your trains (aka a "Throttle")


 \*A computer is optional for making a USB connection and using programs like WebThrottle or JMRI and to update/add EXRAIL Scripts to the |EX-CS|. A USB connection also provides a connection to a "serial monitor" to generate logs and diagnose issues, but more on that later.

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

.. XXX Add link above to point to the full manual

* Track connected to Track A Output
* Power supply input connected to Power IN DC barrel jack

And to connect via WiFi to the EX-CSB1 to control trains your smart device will need either:

* Engine Driver or EX-ToolBox for Android
* WiThrottle for Apple iOS

.. NOTE:: 
   There are quite a few custom features in Engine Driver and EX-Toolbox. It may be worth getting a cheap Android phone or tablet just to be able to use those apps


Connecting to the EX-CSB1 via WiFi:

* Select the WiFi network in your smart device wifi settings named ``DCCEX_xxxxxx``, and use the corresponding password ``PASS_xxxxxx`` (where xxxxxx is identical in each case) shown on your EX-CSB1's OLED display
* Tell your smart device not to worry about there being no Internet connection
* Launch throttle app, which should connect automatically
* You may need to tell your smart device to not automatically connect to your default network or it might keep trying to reconnect to that instead

These quick tips may actually be enough to get your running, but step by step instruction follow below.

Track Connection
-----------------

There are 2 track output power connectors marked A and B. In the standard DCC-EX configuration of a CSB1, A is configured for DCC **MAIN** operation, and B is configured for **PROG** or programming track output. We recommend connecting your track to the A MAIN output initially to test your Command Station. 

To alter this default configuration of DCC outputs, or for DC Mode, you would need to configure outputs with a TrackManager command in the mySetup.h file or via Routes. See :doc:`the TrackManager page </trackmanager/index>`

.. figure:: /_static/images/ex-csb1/ab_outputs.png
   :alt: Track A and B Outputs
   :scale: 90%
   :align: center

   Track A and B Outputs

The pluggable male screw terminals accept to 16 to 28 AWG/1.5mm^2 gauge solid or stranded wire. If you use stranded, we recommend "tinning" the ends of the wire to make a good connection and ensure that stray wire whiskers don't stray outside the screw terminals and cause a short circuit. Larger wire can handle more current and provide less resistance.  18-22 AWG usually good. Keep your wires short by mounting the CS close to the track. 

.. todo See XXX for more information or wire gauge.

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

Connect the other ends of the track output wires to your track. While not critical at this stage when using DCC, it is best to keep to a standard where the RED wire (or striped wire) is connected to the outside rail of the track to make things easier when using feeders to track sections or adding reversing loops. 

.. todo XXX need to mention DC here with a link?

.. figure:: /_static/images/ex-csb1/track_power_conn_1.jpg
   :alt: Connecting Wires to Track
   :scale: 80%
   :align: center
   
   Connecting Wires to Track

.. todo Add more on WiFi here XXX and More on this below XXX

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

To fully power the CSB1, just plug your power supply into the mains power (aka wall outlet) and connect the barrel end to the Command Station. Make sure your power supply matches the needs of your setup: the voltage should be between 12V and 25V DC, depending on the scale of your locomotives, and it should provide at least 2A of current with good over-current performance and voltage stability. To get the most out of your EX-CSB1, we suggest using a modern switching power supply with 4A or more. For Z scale, 12V is usually enough, but for N, HO, and OO scales, we recommend using between 14V and 16V DC. It's important that your DC power is well-regulated which is why we suggest a modern switch-mode power supply with double insulation and strong overload protection.

.. figure:: /_static/images/ex-csb1/csb1_barrel_insert.png
   :alt: Inserting barrel plug
   :scale: 40%
   :align: center

   Inserting Power Supply Barrel Plug

When you connect power to the CSB1 via the barrel connector, you should see both bright green power LEDs light up (5V and 3.3V power), confirming that the electronics are working. However, for safety, track output power will be off by default when you first plug in the EX-CSB1. This is to prevent power from accidentally being applied to your layout before everything is ready. If you prefer, you can change this default setting in the :doc:`Startup Configuration </ex-commandstation/advanced-setup/startup-config>` ). 

.. figure:: /_static/images/ex-csb1/csb1_power_barrel.png
   :alt: Barrel Power LEDs
   :scale: 40%
   :align: center

   Barrel Plug Power LEDs

You should see status information on the display including the CSB1 firmware version, track power status, free memory, and WiFi connection information. If you do not have a display, you will need to connect a serial monitor (See: :doc:`Using a Serial Monitor </reference/tools/serial-monitor>`).

.. todo XXX insert link to serial monitor

.. figure:: /_static/images/ex-csb1/csb1_oled.png
   :alt: OLED Status Display
   :scale: 40%
   :align: center

   OLED Status Display

Connect the Smart Device to the CSB1 AP Network
-------------------------------------------------


The DCC-EX EX-CSB1 Command Station/Booster will power up in WiFi Access Point mode as configured out of the box, with a Wifi network SSID of DCCEX_xxxxxx and password of PASS_xxxxxx (where xxxxxx is the last 6 digits of the MAC address of the CSB1), both of which will be visible on the OLED display (or serial monitor log) after it boots so you can connect with a WiFi throttle like Engine Drive or WiThrottle. This quick start covers initial testing with a WiFi smart device app, for a USB Connection with EX-WebThrottle or JMRI and a computer, please see the full :doc:`CSB1 operating manual <manual>`.

Access Point (AP) mode creates a separate WiFi network on the Command Station itself, whereas Station (STA) mode allows the Command Station to join as a WiFi device on your home or layout WiFi network. We have the EX-CSB1 set to default to AP mode for convenience of being able to get up and running quickly. To configure your CSB1 to connect to your network, see :doc:`WiFi Configuration </ex-commandstation/advanced-setup/supported-wifi/wifi-config>`.

The WiFi LED will illuminate once WiFi is configured and ready as an Access Point (or Station if reconfigured for STA mode.)

On your device, select the network settings and find an available network that begins with "DCCEX\_".

.. figure:: /_static/images/engine_driver/ed_wifi_select1.png
   :alt: Smart Device Available Network Screen
   :scale: 40%
   :align: center

   Smart Device Available Networks Screen

Click on that network to see the next screen to enter your password. Notice the password is just "PASS\_" followed by the same 6 digits in the network name (called a "SSID").


.. figure:: /_static/images/engine_driver/ed_wifi_pass.png
   :alt: Smart Device AP Password Entry
   :scale: 40%
   :align: center

   Smart Device AP Password Entry

.. todo XXX We need to probably link to the manual or another CSB1 doc and cover using installer as preferred to the IDE


.. todo [insert link] XXX figure link showing WiFi LED

Log Engine Driver into the CSB1 AP Network
-------------------------------------------

Open the Engine Driver App on your Android smart device: 


.. figure:: /_static/images/engine_driver/ed_ed_icon.png
   :alt: Engine App Icon
   :scale: 45%
   :align: center

   Engine Driver App Icon

Once loaded, select your preferences when the Intro/Setup wizard launches. You can skip to the next paragraph if you see the "Welcome to Engine Driver" Wizard screen. If you have already used Engine Driver, you can run the wizard again from the app menu:

.. figure:: /_static/images/engine_driver/ed_preferences1.png
   :alt: Engine Driver App Menu
   :scale: 45%
   :align: left

   Engine Driver App Menu


.. figure:: /_static/images/engine_driver/ed_wizard_menu.png
   :alt: Engine Driver Intro/Setup Wizard
   :scale: 45%
   :align: center

   Engine Driver Intro/Setup Wizard

The Wizard allows you to set or change appearance options and, most importantly, choose to use DCC-EX native commands instead of WiThrottle:

.. figure:: /_static/images/engine_driver/ed_wizard1.png
   :alt: Engine Driver Wizard Opening Screen
   :scale: 45%
   :align: center

   Engine Driver Wizard Opening Screen

Scroll through the other screens setting your preferences until you get the the DCC-EX screen and make sure to select the option to use an EX-CommandStation

.. figure:: /_static/images/engine_driver/ed_wizard6.png
   :alt: Engine Driver Wizard DCC-EX Select
   :scale: 45%
   :align: center

   Engine Driver Wizard DCC-EX Select

Next, select the "preferences" option:

.. figure:: /_static/images/engine_driver/ed_preferences2.png
   :alt: Changing Engine Driver Preferences
   :scale: 45%
   :align: center

   Changing Engine Driver Preferences

In order to get the most functionality from Engine Driver, there are a few settings that should be changed. By default, Engine Driver uses the WiThrottle protocol, which the EX-CSB1 also understands, but the native DCC-EX protocol has much more power. Scroll through the long list of options and make sure "Emergency Stop", "Layout Power Button" and "DCC-EX Button" are all checked


.. figure:: /_static/images/engine_driver/ed_preferences3.png
   :alt: Engine Driver optional buttons
   :scale: 45%
   :align: left

   Engine Driver optional buttons

   

.. figure:: /_static/images/engine_driver/ed_preferences4.png
   :alt: Engine Driver DCC-EX button option
   :scale: 45%
   :align: left

   Engine Driver DCC-EX button option

|BR|

Keep scrolling to see the option for "DCC-EX - EX-CommandStation Preferences" and click on it. Then choose "Auto" or "Yes". Auto will automatically switch between WiThrottle protocol for other command stations and DCC-EX protocol when Engine Driver sees it is a DCC-EX command station. If you aren't using other command stations, at home or at a club, simply choose "Yes".

.. figure:: /_static/images/engine_driver/ed_dccex_preference1.png
   :alt: Engine Driver DCC-EX button option
   :scale: 45%
   :align: left

   Engine Driver DCC-EX button option

.. figure:: /_static/images/engine_driver/ed_preferences5.png
   :alt: OLED Status Display
   :scale: 45%
   :align: center

   OLED blah


Confirm startup
----------------

todo XXX [insert link] Show and explain the startup screen

Turn On Track Power
--------------------

Show how to slide the power slider, etc

Run a locomotive
------------------

reverse this and power? when to put loco on track? todo XXX

DCC Operation
---------------

The EX-CSB1 is set to operate in DCC mode by default. If you want to switch to any of the outputs to DC mode, you can find instructions on how to do that here :doc:`TrackManager page </trackmanager/index>`

Booster Mode
--------------

The |EX-CSB1| as the name implies can operate as a Command Station or a Booster. See [insert link] for instructions on how to use the EX-CSB1 as a booster.

Full EX-CSB1 Operating Manual
------------------------------

[insert link]
