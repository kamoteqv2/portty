# portty

Portty.exe is a small and handy utility application designed to help you connect your Arduino Uno board to your PC. With this app, you can easily manipulate the output pins and change their state to on or off as per your needs. Additionally, if you have a DHT sensor connected to pin 2 of the Arduino board, you can use Portty.exe to fetch the temperature and humidity data from the sensor.

Not only that, but Portty.exe can also be used to test your Arduino board or control external electrical devices using appropriate switching relays. By connecting the relays to the output pins of the Arduino board, you can use Portty.exe to change the state of the relays and thus control the connected devices. This makes Portty.exe a versatile tool for controlling a wide range of devices in various projects, whether for testing purposes or for real-world applications.

To use Portty.exe, simply flash your Arduino Uno with the included hex file. There are three hex files available for different DHT models, and you can use the xloader utility to upload the Portty hex to the board.

Starting the connection between Portty.exe and the Arduino board is quite straightforward. All you need to do is run the following command line in your terminal:

```
portty.exe <board-name> <com-port-number>
```

Example:
```
c:\portty>portty.exe myboard com11
```

```
Status     : Connected
Serial Port: com11
Baud Rate  : 9600
Board Alias: myboard

Help       : ?
Exit       : x

Toggle Pin Number:
```

To toggle the pin status of pin 4, and if the current status is 0, this will set inverse pin status to 1
```
Status     : Connected
Serial Port: com11
Baud Rate  : 9600
Board Alias: myboard

Help       : ?
Exit       : x

Toggle Pin Number: 4

pin state change to 1

Press Enter key to continue...
```

and if you enter the same pin number this will inverse the pin status again to 0

```
Status     : Connected
Serial Port: com11
Baud Rate  : 9600
Board Alias: myboard

Help       : ?
Exit       : x

Toggle Pin Number: 4

pin state change to 0

Press Enter key to continue...
```


if you press the key ****?***

```
Syntax   : portty.exe <board-name> <com-port>
Example  : portty.exe myboard com5

s        : Pin Status
t        : Temperature
h        : Humidity

pin 2    : DHTxx sensor
pin 3    : LED Power Indicator
Free Pins: pin 4 to 19

Press Enter key to continue...
```
and pressing
****s**** will give you the complete board values
****t**** temperature from the dht sensor
****h**** humidity from the dht sensor

**Note**
- pin 2 is reserved for DHT signal pin
- pin 3 optional, can be use to connect to a LED as power and activity indicator
- and pin 4 to 19 are available for toggling or switching 
