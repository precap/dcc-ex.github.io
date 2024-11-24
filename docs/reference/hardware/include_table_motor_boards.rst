.. include:: /include/include_xb.rst
  
.. list-table::
  :widths: auto
  :header-rows: 1
  :class: command-table

  * - Motor Board Type / Brand
    - Recom- |BRxb| mended
    - Sup- |BRxb| ported
    - Comfort |BRxb| Level
    - Format
    - Stackable
    - Short |BRxb| Circuit |BRxb| Protection
    - Current |BRxb| Sense [20]_
    - DC |BRxb| Support
    - No. Outputs
    - Max Amps |BRxb| (per output)
    - Comments / Notes . . . . . . . . . . . . . . . . . . . . . . . . . . 

  * - :doc:`DCC-EX EX-MotorShield8874 RevA</reference/hardware/motorboards/ex-motor-shield-8874>`
    - Yes
    - Yes
    - Tinkerer
    - UNO / Mega
    - Yes [21]_
    - Yes
    - Yes
    - Yes
    - 2
    - 5
    - 

  * - :doc:`Arduino Motor Shield R3</reference/hardware/motorboards/arduino-motor-shield>`
    - Yes
    - Yes
    - Tinkerer
    - UNO / Mega
    - No
    - Yes
    - Yes
    - Yes
    - 2
    - 1.3 - 1.5
    - 

  * - :doc:`Deek-Robot Motor Shield</reference/hardware/motorboards/deek-robot-motor-shield>`
    - No
    - Yes
    - Tinkerer
    - UNO / Mega
    - No
    - Yes
    - Yes
    - Yes
    - 2
    - 1.3 - 1.5
    - 

  * - :doc:`Flashtree Motor Shield</reference/hardware/motorboards/flashtree-motor-shield>`
    - No
    - Yes
    - Tinkerer
    - UNO / Mega
    - No
    - Yes
    - Yes
    - Yes
    - 2
    - 1.3 - 1.5
    - 

  * - :doc:`DIY More L298NH</reference/hardware/motorboards/diy-more-l298nh-motor-shield>`
    - No
    - Yes
    - Tinkerer
    - UNO / Mega
    - No
    - Yes
    - Yes
    - Yes
    - 2
    - 2
    - 

  * - :doc:`YFRobot L298P</reference/hardware/motorboards/yfrobot-l298p>`
    - No
    - Yes
    - Tinkerer
    - UNO / Mega
    - No
    - No
    - No
    - No
    - 2
    - 2
    - 

  * - :doc:`L298N (dual)</reference/hardware/motorboards/L298N-motor-board-setup>`
    - No
    - Yes
    - Engineer
    - 
    - No
    - No
    - No
    - No
    - 2
    - 2
    - It doesn't have current sense

  * - :doc:`Dual Module H-bridge MOSFET IRF3205</reference/hardware/motorboards/IRF3205-motor-board-setup>`
    - No
    - Yes
    - Tinkerer
    - 
    - No
    - No
    - No
    - No
    - 2
    - 15
    - 

  * - :doc:`Pololu MC33926</reference/hardware/motorboards/pololu-mc33926>`
    - No
    - Yes
    - Tinkerer
    - UNO / Mega
    - No
    - No
    - No
    - No
    - 2
    - 3
    - current sense is not acceptable. We recommend using an external current sense board like the MAX471

  * - :doc:`MiniIBT L6201P (single)</reference/hardware/motorboards/miniibt-motor-driver-l6201p>`
    - No
    - Yes
    - Tinkerer
    - 
    - No
    - No
    - ?
    - No
    - 1
    - 5
    - 

  * - :doc:`BTS7960 IBT_2 (single)</reference/hardware/motorboards/IBT_2-motor-board-setup>`
    - No
    - Yes
    - Tinkerer
    - 
    - No
    - No
    - ?
    - No
    - 1
    - 43
    - 

  * - :doc:`Keyes/Fundumoto ("Beeper Board")</reference/hardware/motorboards/keyes-fundumoto>`
    - No
    - Yes
    - Engineer
    - UNO / Mega
    - No
    - Yes [22]_
    - Yes [22]_
    - No
    - 2
    - 2
    - 

  * - :doc:`Makerfabs H-Bridge</reference/hardware/motorboards/makerfabs-h-bridge-motor-shield>`
    - No
    - Yes
    - Engineer
    - 
    - No
    - No
    - No
    - No
    - 2
    - 8
    - 

  * - :doc:`Velleman KA03/VMA03</reference/hardware/motorboards/velleman-ka03-kit-vma03>`
    - No
    - Yes
    - Engineer
    - 
    - No
    - No
    - No
    - No
    - 2
    - 2
    - 

  * - :doc:`DFRobot 2x2A DC Motor Shield (DRI0009)</reference/hardware/motorboards/dfrobot-2x2a-dc-motor-shield>`
    - No
    - Yes
    - Engineer
    - UNO / Mega
    - No
    - No
    - No
    - No
    - 2
    - 2
    - 

  * - VNH2SP30 - SparkFun Monster Moto and others
    - \-
    - :dcc-ex-red-bold-italic:`No`
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - Does not work. It can't switch fast enough to generate a reliable DCC signal

  * - IFX9202ED - Infineon Dual H-Bridge
    - \-
    - :dcc-ex-red-bold-italic:`No`
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - Does not work. Can't switch fast enough.

  * - DFRobot Romeo V2
    - \-
    - :dcc-ex-red-bold-italic:`No`
    - Engineer
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - Well, an Engineer could perhaps get this one to work.

  * - Kuman Board (and any L293D based boards)
    - \-
    - :dcc-ex-red-bold-italic:`No`
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - Does not work. Not enough current.

  * - Pololu TB9051FTG based motor shield
    - \-
    - :dcc-ex-red-bold-italic:`No`
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - \-
    - Does not work. It can't switch fast enough to generate a reliable DCC signal


.. [20] CV Programming
.. [21] Requires modification of the board to stack the second board
.. [22] Requires modification of the board to support Current Sense
