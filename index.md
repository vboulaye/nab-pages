## Welcome to Nabaztag Pages

Make your rabbit great again.

You found an old nabaztag that is not able to do anything.
Follow this step to revive it

### Install the WPA2 firmware

The Nabaztag:Tag (V2) only support WEP or WPA encryption for the WiFi connection.
A custom firmware as been developped by @RedoXyde that add Wpa2 support.
The firmware file `Nab0013.01ca89.sim`  is available here: https://github.com/RedoXyde/nabgcc/releases/

Installation process:
- start the nabaztag in configuration mode (press the head button when plugging it in)
- the leds go blue and a SSID wifi in `nabaztag##` appears
- connect to it (the dhcp does not work well, I had to give myself a static ip on its network, 192.168.0.11 for example)
- open the url http://192.168.0.1
- the administration page is displayed
- click on "Click here for firmware upgrade"
- select the file of the firmare + click on "upload"
- wait for the reboot (the leds go first to red and then to orange as the WiFi setup is not done).
- restart the nabaztag in configuration mode and reconnect to its wifi network
- go to the configuration page of the wifi: follow the link "click here to start"
- select or entter your ssid (warning the ssid typed in the textbox has priority over the one selected from the dropdown)
- choose wpa2
- enter your wifi password
- click on "update and start"
- in principle if the connection goes well we get 2 green leds and 2 oranges, one flashing then everything goes to orange, because the Violet server configured by default is now down...

You can now continue to http://openjabnab.fr if you want to setup your nabaztag with it.

But if you'd prefer an 'autonomous' rabbit you can configure it to use...

# Serverless Nabaztag server

This "firmware" (actually the piece of code downloaded and executed at startup by the Nabaztag) can expose a web API directly on the rabbit.

It comes from the project https://github.com/andreax79/ServerlessNabaztag forked to https://github.com/vboulaye/ServerlessNabaztag just to change the accent of generation of text2spech to French. 

To install it you have to deploy it on a web server, or use the files deployed on this site, then configure the rabbit:
- start the rabbit in configuration mode
- click on "click here to start"
- click on "advanced configuration"
- At the bottom of the page change the purple platform url to the location of the bc.jsp file from ServerlessNabaztag for example `192.168.1.25/vl` (without the http://)
- click on "update and start"
- in principle you get 4 green LEDs then a single pulsating under the rabbit

- look for the ip of your rabbit on the network

