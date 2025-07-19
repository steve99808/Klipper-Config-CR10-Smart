The stock CR10 Smart was a bit of a pain to use, so I decided to rebuild it. 
Motherboard is a Bigtreetech SKR Mini E3V3 and a Raspberry Pi Zero 2W for Klipper, a Linear Rail on the X-Axis and a BIQU Microprobe for Mesh Bedleveling. 

For connecting the RasPi Zero with the BTT SKR Mini E3 V3 you need to switch the TX & RX connections from the Raspberry to the TFT connection at the BTT board. 
Installed Klipper according to the Klipper website. 

For the mechanical parts I drilled straight into the X-carriage and changed the position of the endstop. For using a Voron Stealthburner I used an <a href="https://www.printables.com/model/913817-linear-rail-mount-for-voron-stealthburner-on-ender?lang=de">adapter</a> which was originally made for the Ender 3, what worked perfectly. 
STLs for the Stealthburner you can find in the Voron repository. 

After Leveling it works pretty well, but there are some issues I'm currently working on.
Issues: 
-Overheating of the Raspberry Pi 
Solution: Connecting extra Fans at the GPIO Pins
Upcoming changes:
-Y-Axis linear rails
-Camera with AI failure detection

Update 1.1
My Raspi shorted out so I switched it out with a BTT PI V1.2. Pros of it were the option for a LAN and USB conncection, which made it more like Plug&Play and makes it easier for connecting a Camera for my future upgrades.
Only issue I had was with WiFi, which was sorted out pretty quick after connceting it with LAN and SSH, sudo nmtui, enable and connect the WiFi connection there. 
After that it was the regular Klipper installation. Just need to change the motherboard connection in the printer.cfg. 
You find it in SSH with "ls dev/serial/by-id/". Copy the prompted out serial connection and paste it in your printer configuration in Mainsail. 
