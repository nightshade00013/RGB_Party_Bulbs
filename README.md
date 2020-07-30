# RGB_Party_Bulbs
This is a NodeRED flow that will allow you to have your RGB HomeAssistant lights shift colors on a loop until you turn it off the off function is the same script as is used to turn it on.

For those wondering how this will look and work check out the video here:  https://youtu.be/vAGbYbFNgC0

If you found this project helpful and want to throw a few bones my way I would greatly appreciate it. You have a couple options to do so. One is to make a purchase on Amazon using my affiliate link, donate through buy me a coffee, or toss a couple Satoshi to me using Bitcoin.

https://amzn.to/2v74aiY Amazon affiliate link, any purchases made after clicking this will help support the author. https://www.buymeacoffee.com/Slw0NRx donation link through Buy Me a Coffee. 17pEPchqZrjVHv8oN3jKMDZp23A24j4Jj Bitcoin address for direct anonymous gifts.

So this uses some Tuya Based bulbs to cycle through a pleasant color shift.  I think this would be nice to keep a child entertained or useful if you are throwing a party and will have some music playing or whatever.


This is placed for use by others who may be interested and want to try it. It comes with no support or guarantee.

This uses NodeRed, Home Assistant, and ESPHome flashed using Tuya-Convert.

https://www.home-assistant.io/ Home Assistant.

https://nodered.org/ NodeRed.

https://github.com/ct-Open-Source/tuya-convert Software to flash bulbs to ESPHome.

https://esphome.io/ ESPHome main page.


Outside of the inbuilt nodes I used the used nodes node-red-contrib-home-assistant-websocket and node-red-contrib-toggle

I setup an empty script to trigger the function in HomeAssistant and pulled the function out to only the one I needed.  Changed the output to a simple command and put in a toggle switch.  A Javascript to break the loop and a simple off plus a delay if the first one doesn't actually turn it off.  The rest of it is basically setting the colors and a delay between.  This one uses a base color plus a step between so that is why some of the delays are slightly longer than the others.  ESPHome does the transition over about a second by default and visually the delays I put in made it seem like the stops and transitions were just about the same.  Currently all I am doing is full colors but it transitions nicely from blue to pink to red to yellow to green to aqua and then repeats the loop.  The one thing not shown in the screenshot is I had to add a filter so they only get the stop trigger for the stop sequence.

And when setting up the empty script you can get most everything from here on how to make it work https://bonani.tech/how-to-trigger-a-node-red-flow-from-the-home-assistant-ui/ 
