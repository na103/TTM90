# Videotel TTM90 RS232 mod
the TTM90 (Multistandard Telematic Terminal) is a Videotel produced by the Italian company Italtel in the 1990s.<br>
It is a rugged product, well designed and with a beautiful design.<br><br>

![alt text](https://github.com/na103/TTM90/blob/main/img/ttm90.jpg)

As far as I know there are two versions of TTM90:<br>
the TTM90 "basic" where the only interface present is the parallel one, no communication port, it only has the modem.<br>
the TTM90/TL equipped with a minitel plug DIN 5 communication interface where in theory (I haven't tried)<br>
it should be possible to use a wifi modem like [this](https://p-l4b.github.io/minitel/)<br>
<br>
this is a step by step guide on how to add the rs232 serial interface to the TTM90 "basic" version and how to configure it to connect using the interface<br>
the logic board provides the possibility of installing RS232 as an option.<br>
no major changes are necessary, just add the following components as shown in the picture below:<br><br>
![alt text](https://github.com/na103/TTM90/blob/main/img/board.png)
<br>
## list of component
Solder wire traces into the locations 09,10,12,16,21,22,23,24,25,26,27,28,31,32,37,38,39<br>
n°3 100nF 50V ceramic capacitor C02,C09,C12<br>
N°2 1N.4007 diode D03,D04<br>
N°1 MC1488 U05<br>
N°1 MC1489 U03<br>
N°1 RS232 25 pin male<br><br>
in the end your work should look like this:<br><br>
![alt text](https://github.com/na103/TTM90/blob/main/img/rs232mod.jpg)<br>
## Building notes
be careful, for some strange reason (probably a design error) the pinout of the 25 pin rs232 interface is flipped.<br>
you will have to build a special cable or use a jumper box adapter.<br>

![alt text](https://github.com/na103/TTM90/blob/main/img/rs232adapter.png)

## TTM software configuration
once the hardware modification has been completed, it is necessary to enable the interface from the configuration menu.<br>
at power on enter the access code (press the space key 5 times) to unlock the hidden configuration menu:<br>

![alt text](https://github.com/na103/TTM90/blob/main/img/confmenu.png)

<br>

now in the "serial interface programming" submenu choose "rs232" and set the speed and format.<br>

![alt text](https://github.com/na103/TTM90/blob/main/img/setupint.png)
<br>
after having done this you will be able to access the dialing directory and without setting any telephone number you will be able to set the serial interface, parameters and type of terminal emulation.
<br><br>
If you found this my work useful, please consider buying me a cup of coffee if you want:<br>
<a href='https://ko-fi.com/na103' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/cup-border.png' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>
## Thanks
Thankyou to all the people who have helped with this project.<br>
[Claudio](https://p-l4b.github.io/) for providing "the two carabinieri" (mc1488/mc1489) and help me in reverse engineering.
## License
This work is licensed under a Creative Commons Attribution 4.0 International License. See [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

