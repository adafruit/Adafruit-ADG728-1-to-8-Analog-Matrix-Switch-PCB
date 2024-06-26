## Adafruit ADG728 1-to-8 Analog Matrix Switch - Stemma QT PCB

<a href="http://www.adafruit.com/products/5899"><img src="assets/5899.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit ADG728 1-to-8 Analog Matrix Switch - Stemma QT. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/5899

### Description

Analog switches are a solid state alternative to relays, when you want a smaller, lower-power technology that won't wear out mechanically. And, as the name implies, you can use the Adafruit ADG728 1-to-8 Analog Matrix Switch to connect between eight analog signals, much like a set of 8 mechanical switches. These chips tend to be tiny surface mount parts, so this breakout will let anyone use the ADG728 switch for signals up to 5V, without fiddly soldering.

The ADG728 uses I2C to select which of the 8 channels switches to turn on or off, to connect that channel to the single analog 'D' pin Note that unlike digital switches and multiplexers, these are not 'input' and 'output' because the signal is bidirectional. You could have the D signal be an input to 8 outputs, or the 8 inputs to one output.

Also, the ADG728 isn't really a 'selecting multiplexer', its a matrix switch with 8 independent switches. That means that yes, you could treat it like an SP8T where you select which signal is routed to the D pin, you can also turn on multiple switches to 'merge' the signals together. 

Unlike a relay or mechanical switch, analog switches don't wear out, and the switch time is near instant, about 100nS. The ADG728 chip also guarantees break-before-make so the deselected switches will open before selected switches close.

However, there's a few things to watch out for:

* The VIN power pin (the red wire if using a STEMMA QT cable) must as high as the highest analog voltages you want to switch. That means if the analog signals are no more than 5VDC, the V+ pin must be higher than 5V. You cannot power this pin with 3.3V and switch 5V signals.
* It cannot switch signals below ground. No negative voltages can be applied to the Switch or D pins!
* Analog switches are for signals, not power! Since this is not a mechanical switch, the signals pass through circuitry that is not designed to source or sink current. This is great for analog signal voltages, and is not good for providing more than a few mA of current.

In addition to the 8 switch S pins and the D pin that can be switched to, there's also two I2C address pins so you can change the default address from 0x4C up to 0x4F. There's also a reset pin if you want to immediately set all the switches to open.

To get you going fast, we spun up a custom-made PCB in the STEMMA QT form factor, making it easy to interface with. The STEMMA QT connectors on either side are compatible with the SparkFun Qwiic I2C connectors. This allows you to make solderless connections between your development board and the ADG or to chain it with a wide range of other sensors and accessories using a compatible cable.

### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
