# rf-jammer
Professional RF jammer with RF VCO and power RF amplifier

This is a desription how professional RF jammers are being made. They are using Sawtooth/Triangle wave generator combined with Voltage Controlled RF Oscillator and Power output stage RF amplifier.

If you intend to build a UAV / drone / quadcopter jammer remember that you need to make 3 of such units for the bands GPS ( 1575 MHz) , 2.4GHz WiFI , 5.8 GHz WiFi. Each of such jammers needs to have its own power amplifier and antenna and VCO for different frequency, however all 3 of them can be connected to single sawtooth/triangle signal generator. 

When choosing right RF power amplifier please search for something with heatsink and QORVO company TQP7M9103 / TQP7M9105 chip : https://www.qorvo.com/products/p/TQP7M9103   or at least TQP7M9028 / RQP7M9101. Remember that the capacitors , coils and resistors need to fit the particular frequency  apliance from the vendor - there are different setups for each center RF frequency - check the Bill of Material pages of attached PDF. 

The USB RF VCO I was using is build with YSGM 151708 chip from chineese company INNOTION.  http://www.innotion.com.cn/VCO

these chips can be bought here https://txtelsig.en.made-in-china.com/product/twLGguvjXPWl/China-High-Quality-2g-3G-4G-5g-WiFi-GPS-Vco-Voltage-Controlled-Oscillator.html

The video showing my attempt to build simple GPS jamming device is available here : https://youtu.be/sZCd-gE_p84?si=8e9XHNKYu6v522VL




