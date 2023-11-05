# magic-mirror
A collection of hardware and software to create an amazing magic mirror for your smart home.

## Showcase 

I have hung a Magic Mirror in my hallway and made it touch-enabled. 
It works with a special monitor that supports "touch through glass" and a spy mirror that is touch-permeable.
The Magic Mirror software runs as an iframe in a Home Assistant dashboard, so you can also control your whole smart home with it.

Have a look at the [showcase video](https://www.youtube.com/watch?v=HoU3uVTFj8k) to see it in action.

[![Showcase Video](https://img.youtube.com/vi/HoU3uVTFj8k/0.jpg)](https://www.youtube.com/watch?v=HoU3uVTFj8k)

Apart from the fingerprints and Siri, I am very satisfied ;)

## Hardware:

The most difficult thing was to find a suitable screen and spy mirror that would still allow touch. 

- Raspberry Pi 4 (will probably upgrade to a pi 5 soon because of the better performance)
- [Iiyama Touch Monitor](https://iiyama.com/de_de/produkte/prolite-tf2234mc-b7x/) (it's important that you choose one that supports "Touch through glass")
- [Spy Mirror](https://www.glas-star.de/pages/smart-mirror-glas) (afaik only the MirroView™ from Pilkington is touch-permeable. I use the 4mm version)
- [Wall mount](https://amzn.eu/d/0x3sJC1) (I use additional 3d printed parts to fix the mirror in front of the monitor without the need of a frame) 



## Software:

### Magic Mirror

I'm using the famous [Magic Mirror software platform](https://magicmirror.builders/) with a lot of different modules.

- [Home Assistant Display](https://github.com/wonderslug/MMM-HomeAssistantDisplay)
- [SmartTouch](https://github.com/EbenKouao/MMM-SmartTouch)
- [MMM-Remote-Control](https://github.com/Jopyth/MMM-Remote-Control)
- ... and many more

### Home Assistant

To easily display more information on the screen than the Magic Mirror software and its modules are capable of and to control the smart home, I use [Home Assistant](https://www.home-assistant.io/)

The Magic Mirror is displayed in an iframe inside a Home Assistant Dashboard. This way you can easily switch between different dashboards and control your smart home. In addition the displayed content is automatically switched depending on several events. 

- When someone rings the doorbell, the camera is displayed. 
- When the vacuum cleaner is running, the map is displayed. 
- When music is playing, the media player is displayed.

To achieve this, I use the following addons and integrations inside Home Assistant:

- [Browser Mod](https://github.com/thomasloven/hass-browser_mod) (for automatic switching to certain dashboards)
- [WebRTC Camera](https://github.com/AlexxIT/WebRTC) (for displaying the camera)
- [Xiaomi Cloud Map Extractor](https://github.com/PiotrMachowski/Home-Assistant-custom-components-Xiaomi-Cloud-Map-Extractor) (for displaying the vacuum cleaner map)
- [Owntone Media Server](https://github.com/owntone/owntone-server) (for displaying the media player)
- and much more

