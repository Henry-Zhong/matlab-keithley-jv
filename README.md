#Matlab program for J-V measurements with a Keithley 24XX sourcemeter
This project contains device drivers and a corresponding class object for controlling a Keithley 24XX sourcemeter in Matlab. The implemented methods include standard current-voltage measurements, time resolved current-voltage sweep measurements, time resolved current-density point measurements, cyclic current-voltage measurements (MPP->JSC->VOC->JSC), and steady state tracking measurements of maximum power point, VOC, and JSC.

The main function is classKeithley2400.m, which will create a Keithley2400 device object for the Keithley 24XX (SCPI) family. There are two optional input parameters (string connectionType, string/int port), which can be also set after creation. 

All methods are implemented into classKeithley2400_testscript.m and can be tested seperately. For running the program, a GPIB controller is required and the Keithley has to be set to SCPI. A serial connection does not work properly yet, since the Keithley does not allow reading buffered values during the measurement.

Tested: Matlab 2015b, Win10, NI GPIB-USB-HS+ Controller, Keithley KUSB-488B Controller, Keithley 2400, Keithley2410, Keithley2401

Author: Eugen Zimmermann, Konstanz, 2016 eugen.zimmermann [at] uni-konstanz [dot] de

Last Modified on 2016-06-23

Version 1.0

Goals for next version:
- implement exceptions for serial connection
- implement bytesAvailebleFunction for data readings
