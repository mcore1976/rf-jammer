# rf-jammer
Professional RF jammer with RF VCO and power RF amplifier

This is a desription how professional RF jammers are being made. They are using Sawtooth/Triangle wave generator combined with Voltage Controlled RF Oscillator and Power output stage RF amplifier.

If you intend to build a UAV / drone / quadcopter jammer remember that you need to make 4 of such units for the bands GPS ( 1575 MHz) , 2.4GHz WiFI , 5.2GHz and 5.8 GHz WiFi. 
Each of such jammers needs to have its own power amplifier and antenna and VCO for different frequency. 
Each Channel may require to use different triangle/sawtooth generator - another NE555 chip with different Resistors and Capacitors values for each VCO chip and frequency - this is due to different characteristics of VCO modules (check "Frequency vs Tunning Voltage" diagram in YGSM chip PDFs).

When choosing right RF power amplifier please search for something with heatsink and QORVO company TQP7M9103 or SBB5089Z chip  or better: https://www.qorvo.com/products/p/TQP7M9103 , https://www.qorvo.com/products/d/da001309 
Remember that the capacitors , coils and resistors on TQP7M9103 dev kit board need to fit the particular frequency apliance from the vendor. The TQP7M9103 boards from chinese vendors need to be altered, they do not work out of the box.
TQP7M9103 dev kit has different setups for each center RF frequency - check the Bill of Material pages of attached PDF. 
For the SBB5089Z it looks better because it is 50MHz-6000MHz wideband power amplifier which only requires couple of components that do not change along with the frequency.

The USB RF VCO I was using is build with YSGM 151708 chip from chineese company INNOTION.  http://www.innotion.com.cn/VCO
These chips can be bought here https://txtelsig.en.made-in-china.com/product/twLGguvjXPWl/China-High-Quality-2g-3G-4G-5g-WiFi-GPS-Vco-Voltage-Controlled-Oscillator.html or on Aliexpress.

The video showing my attempt to build simple GPS jamming device is available here : https://youtu.be/sZCd-gE_p84?si=8e9XHNKYu6v522VL

In the video I was using following the NE555 triangle signal generator from this page https://www.electroschematics.com/555-triangle-waveform-generator/  with following components along with NE555 : 47nF, 22nF, 100K, 47K. 
The triangle signal frequency was approximately 5KHz. 

For different chips  I would suggest to use following setup : 

a) VCO chip YSGM 151708 ( GPS band 1575 MHz ) - use 4.7nF, 2.2nF, 4.7K, 10K - it gives around 10 meter of GPS jamming range while using only VCO YSGM151708 without additional RF power amplifier. The signal on VTune pin swings between 2V-2.5V which gives jamming in the area 1560MHz - 1590MHz with the frequency 44kHz. 

b) VCO chip YSGM 232508 (Wifi/Bluetotth 2.4GHz band) - use R1=3K, R2=2K, C2 = 4.7nF, C1 = 6.8nF - The signal on VTune pin swings between 1.5V-3.5V which is sufficient to drive VCO around 2.4GHz Wifi/Bluetooth frequency.


Always check PDF for particular YGSM chip and Tuning Voltage diagram. Select carefully resistors for NE555 to achieve output voltage range that maps to the frequency you want exactly jam. 




