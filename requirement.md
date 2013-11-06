# ColaLight Requirements

## Electronics
The electronics design is responsible for the optimisation and charging of a small AA battery as well as the efficient illumination provided by a white LEDs.

### MPPT
When connecting to a supply voltage provided by a standard solar panel, the device needs to maximise the power from that panel. This will be achieved by a maximum power point tracking (MPPT) algorithm. We anticipate that the kind of Photovoltaic panels (PV) used to charge the device will be of the order of just a few watts (2-5W).

### Charger
responsible for safely charging the Lithium Ion battery. This must follow the standard Lion charge cycle - Constant Current followed by constant voltage, making sure maximum voltage is not exceeded. Optionally this could coulomb count for estimating stored charge. We expect the battery to be a minimum of 700 mAhr in an standard AA package. The charging connector should conform to USB device charging standards, but needs to remain flexible in a third world context.


### LED Driver
The led driver will need to efficiently step down the voltage and control the current through the LEDs, A buck based current limited switching model is suggested.

### Phone charge
Optional ability to charge a phone through the USB socket, this is achieved via a switch and a small boost converter to step up voltage from the battery to 5v.

### Specifications
| Feature	| Requirement 	| Description 			|
|---------------|---------------|-------------------------------|
| Light Output 	| 20+ Lumens	| 0.1 square metre @ 25+ Lux	|
| Run time 	| 8+ hours	| @ specified light output	|
| Controls	| LED/OFF/PHONE	| Switch DPDT next to USB	|
| Interface	| USB connector	| Power/charge/discharge	|
| Battery	| 700+mAhr 'AA'	| 700+ mAhr with internal PTC	|

### Additional considerations
- Over-charging and temperature
- Over-discharging and reverse polarity
- Self-discharge
- Environmental impact of batteries
- Battery internal protection
- Charge/Discharge rates
- Availability of all parts for replacement
