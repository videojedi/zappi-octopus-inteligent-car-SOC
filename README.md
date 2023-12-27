# zappi-octopus-inteligent-car-SOC
A home assistant automation to set the octopus inteligent/myenergi zappi integration to the correct required charge amount, based on the car SOC.

When the car is plugged inm the Plug status changes from 'EV Disconnected' to 'EV Connected'.

After a 3 minute delay, the automation will read the the car's SoC and set the Octopus charge limit value to maxVal - SoC. 

maxVal is now set directly from the cars own charge limit value.

Your mobile phone will recieve a notification with the requested charge value.

If the required amount is less than 10%, then a miniumum of 10% will be requested.


## Installation.

Requires the Myenergi, Octopus and Skoda (or other car) integrations to be installed and correctly communicating.

Create a new automation. Click on the three dots (Top Right) and select 'Edit in YAML'.

Copy and paste the code from the example automation.

Change the 'DEVICE ID' tags to your specific devices. 

You'll need to find these entities...

> Myenergi zappi plug status
> 
> Octopus charge limit
> 
> Car battery level
> 
> Car bettery charge limit

and change sensor.enyaq_battery_level to an appropriate sensor for your cars' battery State of Charge.

Save the automation.
