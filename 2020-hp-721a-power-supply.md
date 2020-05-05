# HP 721 Power Supply

I got an old power supply at the local science center.
When I tried it, I noticed the voltage drifts upward until it reaches maximum scale.
I wanted to learn more about it's design and construction, so I decided to repair it.
Fortunately this almost 60-year old power supply has very friendly documentation available.
The HP manual includes sections on "Theory of Operation" and "Service" and a schematic diagram.

## Replace electrolytic capacitors

Original capacitors have date code 1961.  So I new I wanted to replace the electrolytic capacitors.

Order/replace electrolytic "axial" (long) capacitors from [digikey](http://digikey.com)

Capacitor | Original Value | Replacement Value
--------- |-------------- | ------------------
 C2  |  500 uF 75V (big cap) | 470uF
 C3,C4,C5  |  40uf 50V | 47 uF
 C7,C9 |  20uF 50V | 22 uF
 C8 |  4uF 60V | 4.7 uF

Tips from EEVBLOG:
```
C2 can be 470uF and 63V.
Also check C3, C4 and C5."40uF"  50V
Also check the output capacitors C8 and C9.
After this replacement, it should be a fine powersupply :-)
```

## Voltage Drifting
5/2/2020 - replaced caps, but voltage still drifting/climbing

## Notes about repair status:
 * Perhaps Q2 or Q3 amplifier is "drifting" control voltage to Q1 Base, causing power to increase.
 * R20 gets super hot to touch
 * printed HP 721A manual, schematic, made notes about things to try.


## Voltage Reference Upgrade

Stack Exchange topic recommends replace CR7 voltage reference diode.

 * https://electronics.stackexchange.com/questions/179682/how-improve-temperature-sensitivity-of-hp-721a-dc-power-supply-voltage-referencesuggested using LM431 volt ref. with resistor dividers: 
 * http://www.ti.com/lit/ds/symlink/lm431.pdf

But, in this original supply, it seems voltage reference is holding around -7V (not drifting).
Consider upgrading to LM431 for performance, but it probably will not fix this "drifting" symptom.

## Resource Links

* [HP 721A Manual](http://www.hparchive.com/Manuals/HP-721A-Manual.pdf)
* [EEVBLOG Discussion](https://www.eevblog.com/forum/testgear/hp-721a/)
* [3D viewer](http://hpmemoryproject.org/pict/wall_a/anim/721a_q90/viewer.htm)



