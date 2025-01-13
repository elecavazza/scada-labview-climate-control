# scada-labview-climate-control

SCADA Air Conditioning Temperature and Humidity. LabVIEW Server &amp; Client Vis using Global Variables

## Overview

In modern climate control systems, maintaining optimal temperature and humidity is essential
for ensuring comfort and preserving sensitive environments.  
This project aims to simulate a
thermal and humidity control system using LabVIEW.  
The system will monitor ambient temperature and humidity values, process simulated sensor
signals, and regulate environmental conditions by activating a heater or dehumidifier when
values deviate from the desired range.  
The implementation involves three Virtual Instruments (VIs):
- Server VI which implements environment and machine logic
- Global VI for storing, viewing and controlling variables
- Client VI for more limited viewing and controlling
By utilizing global variables and various LabVIEW structures, the system ensures efficient data
sharing, synchronized operation.  
The main objectives of this project are:  
- Develop a Server VI to simulate and control temperature and humidity.
- Implement automatic heater and dehumidifier activation based on setpoint thresholds.
- Display real-time and historical temperature and humidity data, along with system status.
- Create a Client VI for read-only access to data and synchronized sample rate control.
- Ensure smooth data processing using running averages and realistic signal simulations


## How it works

There are three parts to this LabVIEW System.
- The Server Virtual Instrument:
    - semester_1_project_server.vi
- The Global Virtual Instrument:
    - semester_1_project_global.vi
- The Client Virtual Instrument:
    - semester_1_project_client.vi

### The Server Virtual Instrument
The Server Virtual Instrument handles the core operating logic of the system.  
This includes the temperature and humidity simulation along with the heater and dehumidifier
system.  
All states are stored where possible in global variables located within the external Global Virtual
Instrument including controls:  
- Humidity
- Temperature
- Dehumidifier
- Heater
- Humidity setpoint high
- Humidity setpoint low
- Temperature setpoint high
- Temperature setpoint low
- Humidity setpoint high control
- Humidity setpoint low control
- Temperature setpoint high control
- Temperature setpoint low control
- Sample Rate
- Sample Rate Control
- Humidity Max
- Temperature Max
- Power
- Power Control
There is nothing contained within the Server Front Panel.  
The Server initializes all state in the program where possible within a Flat Sequence Structure
outside of the main loop of execution.  
This allows for variables to be initially set with default values within the program before the run
time loop.  