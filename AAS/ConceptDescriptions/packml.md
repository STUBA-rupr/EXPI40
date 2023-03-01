## PackML State Manager Interface

The PackML Interface State Manager is used for communication with the unit/machine from Panels, HMIs or external systems. 
The Interface is used to get status of the unit/machine, start the unit/machine, stop the unit/machine, change parameters, etc.

The PackML Interface State Manager can either be implemented in the same control system (CPU) as the Machine State Manager or in a separate control system. 
A full PackML unit/machine will have one common Interface and one Machine State Manager that is totally integrated with the Machine State Manager.

Related information can be found [PackML State Manager Interface](https://www.omac.org/packaging-workgroup-solutions) and [ISA–TR88.00.02 Machine and Unit States: An Implementation Example of
ISA-88](https://sesam-world.com/_pdf/make2pack/mode/2010-11-29/Materiale/TR_880002.pdf).

### PackML_State_Manager_Interface_TYPE
For this scope only States and Alarms are implemented.

### Administration Tags
Administration tags are used to describe the quality and alarm information of the unit
machine. Administration tags include alarm parameters which describe the conditions within
the Base State model typically for production data acquisition (PDA) systems. The
administration tags also include parameters which can describe how well the machine
operates, or specifically information on the product quality produced by the machine.
Administration tags generally originate from the unit machine and can be used on the HMI or
a remote system.

### Admin.Alarm[#]
Data Type: **Alarm**  
Descriptor: Array of Given Size for Machine Fault Number and Messaging  
The Alarm tags associated with the local interface are typically used as parameters that are
displayed or used on the unit locally, for example from a HMI. These alarm parameters can
be used to display any alarm, or machine downtime cause that is currently occurring in the
system. The alarms are typically limited to the machine unit. The extent of the array is the
maximum number of alarms needed to be annunciated.

### Admin.Alarm[#].ID
Data Type: **INT (32bit)**  
Tag Descriptor: Alarm Message Identification Number  
The Alarm ID number is an unique value assigned to each alarm. The ID can be used for any
general alarms and faults.

### Admin.Alarm[#].Value
Data Type: **INT (32bit)**  
Tag Descriptor: Alarm Message Number  
The Alarm Message number is a value that is associated with the alarm allowing for user
specific detail, or to break down the Alarm.ID to greater detail.

### Admin.Alarm[#].Message
Data Type: **String**  
Tag Descriptor: Alarm Message  
The alarm message is the actual text of the alarm for those machines capable of reading the
string information.

### Admin.Alarm[#].TimeAck
Data Type: **TimeStamp**  
Structure of date and time in the alarm array to detail the date and time the alarm was
acknowledged.

### Admin.Alarm[#].TimeEvent
Data Type: **TimeStamp**  
Structure of date and time in the alarm array to detail the date and time the alarm occurred.

