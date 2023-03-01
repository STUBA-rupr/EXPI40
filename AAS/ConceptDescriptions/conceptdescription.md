## PackML State Manager Interface

The PackML Interface State Manager is used for communication with the unit/machine from Panels, HMIs or external systems. 
The Interface is used to get status of the unit/machine, start the unit/machine, stop the unit/machine, change parameters, etc.

The PackML Interface State Manager can either be implemented in the same control system (CPU) as the Machine State Manager or in a separate control system. 
A full PackML unit/machine will have one common Interface and one Machine State Manager that is totally integrated with the Machine State Manager.

Related information can be found (PackML State Manager Interface)[https://www.omac.org/packaging-workgroup-solutions] and (ISA–TR88.00.02 Machine and Unit States: An Implementation Example of
ISA-88)[https://sesam-world.com/_pdf/make2pack/mode/2010-11-29/Materiale/TR_880002.pdf].



### PackML_State_Manager_Interface_TYPE
For this scope only States and Alarms are implemented.

### Admin.Alarms

### Admin.Alarms

### Status.Alarms