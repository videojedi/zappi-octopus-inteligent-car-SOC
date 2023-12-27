# zappi-octopus-inteligent-car-SOC
A home assistant automation to set the octopus inteligent/myenergi zappi integration to the correct required charge amount, based on the car SOC.

Requires the Myenergi, Octopus and Skoda integrations to be installed and correctly communicting.


When the car is plugged inm the Plug status changes from 'EV Disconnected' to 'EV Connected'.
Your mobile phone will recieve a notification
After a 3 minute delay, the automation will read the the car's SOC and set the Octopus charge limit value to maxVal - SoC. You can set maxVal to the total limit you require. ie 80%.

or if the required amount is less than 10%, then a miniumum of 10% will be requested.

