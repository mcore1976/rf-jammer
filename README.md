# rf-jammer
Professional RF jammer with RF VCO and power RF amplifier

This is a desription how professional RF jammers are being made. They are using Sawtooth/Triangle wave generator combined with Voltage Controlled RF Oscillator and Power output stage RF amplifier.

If you intend to build a UAV / drone / quadcopter jammer remember that you need to make 3 of such units for the bands GPS ( 1575 MHz) , 2.4GHz WiFI , 5.8 GHz WiFi. Each of such jammers needs to have its own power amplifier and antenna and VCO for different frequency, however all 3 of them can be connected to single sawtooh/triangle signal generator. 

When coosing right RF power amplifier please search for something with heatsink and TQP7M9103 chip : https://www.qorvo.com/products/p/TQP7M9103   or better. Remember that the capacitors , coils and resistors need to fit the particular frequency  apliance from the vendor - there are different setups for each center RF frequency - check the Bill of Material pages of attached PDF. 

The video showing my attempt to build simple GPS jamming device is available here : https://youtu.be/sZCd-gE_p84?si=8e9XHNKYu6v522VL




