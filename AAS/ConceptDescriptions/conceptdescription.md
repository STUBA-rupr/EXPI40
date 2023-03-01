## PackML State Manager Interface

The PackML Interface State Manager is used for communication with the unit/machine from Panels, HMIs or external systems. 
The Interface is used to get status of the unit/machine, start the unit/machine, stop the unit/machine, change parameters, etc.

The PackML Interface State Manager can either be implemented in the same control system (CPU) as the Machine State Manager or in a separate control system. 
A full PackML unit/machine will have one common Interface and one Machine State Manager that is totally integrated with the Machine State Manager