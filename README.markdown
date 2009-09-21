
This is a simple breakout board for Xbee radio modem modules.

It was inspired by [Limor's great little Xbee breakout board](http://ladyada.net/make/xbee/index.html).
This one is only a little different in that it is simpler, cheaper, requires only a single-sided PCB
 - which is easier for DIY PCB fabrication - but of course it is significantly less flexible.

However, even though it's less flexible, I think it's perfectly suitable for many common contexts in which you
might use an Xbee module, particularly when interfacing it to a microcontroller such as an Arduino type of thing.

Some surface mount components are used, but surface mount components really don't bite - and I think there is some
merit to having a very simple but useful project involving surface mount components which can serve as an introduction
to surface-mount assembly for beginners.

The connections to this module are bought out to a simple four-pin header, providing the basic requirements of a +5V
power supply, which runs the on-board voltage regulator running the XBee module at 3.3 V, ground, and the UART TX and RX
communications signals, which are intended to be connected to a UART-style interface operating at 5V TTL levels - like an
Arduino or other microcontroller.

Again, we've sacrificed a little bit of flexibility for the sake of simplicity.

I've just bought the 3.3 V level Tx line out of the Xbee module straight out so it can be connected to a 5 V microcontroller
without any kind of level shifting. I've taken the 5 V level data Tx out of the 5 V microcontroller and attenuated it in half
with a simple 1:1 voltage divider and then using this 2.5 V level signal to communicate with the 3.3 V XBee module.

You might think the design described above is inelegant, sub-optimal or just plain dodgy, but in fact, despite being very simple it will work
perfectly well and won't damage anything. In fact, this is precisely the same hardware design used in the official Arduino XBee shield.

The following components will be required:

		1 x XBee radio module
		1 x LM1117-3.3 voltage regulator, surface mount
		2 x LEDs, through-hole 3 mm, pick whatever colours you like.
		2 x 10 k resistor, surface-mount 0805 package
		2 x 69 R resistor, surface-mount 0805 package
		2 x 10 uF 16 V through-hole tantalum capacitors
		2 x 10-pin 2 mm female header sockets
		1 x 4-pin right-angle Molex 0.1" male header



















