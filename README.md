# NSPanel

I'm building a dashboard using a Sonoff NSPanel flashed with ESPHome for Home Assistant.

What I'm using...

**Photoshop** for the main views.  Each room is a view and has 2 main images.  An image with all the buttons off and another with them all on.

**Nextion Editor** to create the layouts.

**Material Design Icons** for the button icons!

The rough idea is that you import the on and off images into Nextion.  Then you add a dual state button in Nextion over the top of the buttons that are part of the background. You remove the text from the button, set the background to "Crop Image" and select the off image for "Picc" and the on image for "Picc2".  This give the impression that you have transparent buttons by revealing just the on image where the button is.

For the Photoshop bit, I'm just importing MD Icons into Photoshop into their own layer and using a color overlay for each layer to change the icon color.  

I'm including the Photoshop files, the icon files, the png files for each room, the HMI file, the YAML file from ESPHome and the TFT file so that you can play around.

This is all provided "as is".  It's not finished yet but someone asked for these so here they are.  I'll try and answer questions but on a best endeavours basis.

This is one example of the background images:

Bedroom off

![BedroomOff](https://github.com/seldomly/acjuksNSPanel/blob/main/roomeron.png?raw=true)

Bedroom on

![BedroomOn](https://user-images.githubusercontent.com/40578133/150555768-5947dfb7-f4b6-4804-b17b-1065144e8efa.png)

In terms of the YAML file, it works.  I think there is a more effiecient way but I'm still getting my head round this.  At the moment, I have sensors to detect the states of the entities in HA.  These are what update the buttons so that if someone switches a light on with Alexa, for example, the button will remain in sync.  What it does mean is that there is a delay in the button state changing.  The light will switch on immediately but the state of the button might take a couple of seconds to update.  I'm ok with that at the moment but it is on the agenda to play around with.
