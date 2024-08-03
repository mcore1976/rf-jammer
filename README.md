# rf-jammer
Professional RF jammer with RF VCO and power RF amplifier

This is a desription how professional RF jammers are being made. They are using Sawtooth/Triangle wave generator combined with Voltage Controlled RF Oscillator and Power output stage RF amplifier.

If you intend to build a UAV / drone / quadcopter jammer remember that you need to make 3 of such units for the bands GPS ( 1575 MHz) , 2.4GHz WiFI , 5.8 GHz WiFi. Each of such jammers needs to have its own power amplifier and antenna and VCO for different frequency, however all 3 of them can be connected to single sawtooth/triangle signal generator. 

When choosing right RF power amplifier please search for something with heatsink and QORVO company TQP7M9103 / TQP7M9105 chip : https://www.qorvo.com/products/p/TQP7M9103   or at least TQP7M9028 / RQP7M9101. Remember that the capacitors , coils and resistors need to fit the particular frequency  apliance from the vendor - there are different setups for each center RF frequency - check the Bill of Material pages of attached PDF. 

The USB RF VCO I was using is build with YSGM 151708 chip from chineese company INNOTION.  http://www.innotion.com.cn/VCO

these chips can be bought here https://txtelsig.en.made-in-china.com/product/twLGguvjXPWl/China-High-Quality-2g-3G-4G-5g-WiFi-GPS-Vco-Voltage-Controlled-Oscillator.html

The video showing my attempt to build simple GPS jamming device is available here : https://youtu.be/sZCd-gE_p84?si=8e9XHNKYu6v522VL

In the video I was using following the NE555 triangle signal generator from this page https://www.electroschematics.com/555-triangle-waveform-generator/  with following components along with NE555 : 4.7nF, 2.2nF, 100K, 47K. 
The triangle signal frequency was approximately 5KHz. 
Finally I would suggest to use following setup : 4.7nF, 2.2nF, 4.7K, 10K - it gives around 10 meter of GPS jamming range while using only VCO YSGM151708 without additional RF power amplifier. The signal on VTune pin swings between 2V-2.5V which gives jamming in the area 1560MHz - 1590MHz with the frequency 44kHz. 

Always check PDF for particular YGSM chip and Tuning Voltage diagram. Select carefully resistors for NE555 to achieve output voltage range that maps to the frequency you want exactly jam. 




