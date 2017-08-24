# Smokey The Barrel
### Automatic temperature controller (ATC) for an ugly drum smoker (UDS)
This ESP8266-based project is controllable via the Blynk smartphone app [over WiFi], reprogrammable OTA, uses 5 k-type thermocouple temperature probes which feed into a PID algorithm, and controls the speed of a 12v DC blower fan via PWM. So many 3 letter acronyms! It pushes the data to [Thingspeak](https://thingspeak.com/channels/164514) and automatically tweets from [@SmokeyTheBarrel](https://twitter.com/smokeyTheBarrel) when certain conditions are met.

<img src="https://github.com/willblev/UDS_ATC/blob/master/img/atc.jpg" height="600" />
<img src="https://github.com/willblev/UDS_ATC/blob/master/img/atc_inside.jpg" height="400" />

### Materials for automatic temperature controller:
- 1x ESP8266 12E module (I used the WeMos D1 mini)
- 5x K type thermocouples & amplifier circuits http://www.ebay.com/itm/181440455042?_trksid=p2060353.m2749.l2649&ssPageName
- 1x 12V DC blower fan with PWM speed control (4 wires)
- 1x 12V power supply
- 1x 12V -> 3.3V DC-DC step down power regulator
- 1x waterproof project box
- 1.5 meters heat-resistant silicone tubing
- 3 L-connectors for tubing
- misc. resistors, wires, and jacks

This project started out as a way to monitor and record the temperature of the smoker and the food, but I've added more and more features (reads as: "broken the code and had to start again") over time. First I got my ESP8266 to work with the temperature probes using the *max6675* library, and was able to post the readings to Thingspeak, doing all this periodically with the *SimpleTimer* library. I then integrated the 12v DC blower fan, which I was able to control with PWM- I set *analogWriteFreq(30000)* as the signal that the fan expected was around 28k-30k. To keep the temperature from oscillating up and down, I integrated the *PID_v1* library. Finally I added OTA capability so that I don't have to take the whole project apart every time I want to tweak the code. 

### The Blynk app (how to control the ATC)
I use the Blynk mobile app to send the desired pit temp and pull temp to the ATC. It can also visualize things like the fan speed, a graph of the last few data points, etc.

<img src="https://github.com/willblev/UDS_ATC/blob/master/img/blynk_app.png" height="600" />

If you would like to clone this project, you can use the following QR code which will copy my Blynk interface which should automatically work with your ATC:

<img src="https://github.com/willblev/UDS_ATC/blob/master/img/blynk_clone.jpg" height="400" />

It is pretty straight forward- you move the sliders left and right to set the pit/pull temp, and the Blynk app sends these changes to the ATC. The ATC updates the app with the current temperature of the pit, the temperature of the food, the fan speed, etc.

### The Ugly Drum Smoker
I cleaned out the inside of the barrel, then I cut off the lid, stripped the paint, and re-painted it with heat-resistant paint. I used six brass 3/4" pipe fittings to provide air flow- three on the bottom as intakes and thee as vents on the top. I used a large steel paellera as a lid, and it rests on the three vents. I also added handles and a modular rack system to adjust the height of the grills inside of the smoker. 

<img src="https://github.com/willblev/UDS_ATC/blob/master/img/UDS.jpg" height="600" />

Find more info and pics about the UDS project [here.](https://trello.com/c/GKH84JZ9/7-uds-ugly-drum-smoker-200l-steel-barrel-bbq-smoker)

### Materials for barrel:
- 1x 200L steel barrel
- 1x wire brush set to remove paint http://www.leroymerlin.es/fp/15520071/set-de-4-cepillos-wolfcraft-metalicos-desherrumbrar
- 6x 3/4'' threaded brass pipe adapters (pairs; male for inside, female for outside)
- 12x 3/4'' steel washers
- ~30x stainless steel bolts and nuts + washers (5-6 mm should be OK)
- 1x 60cm diameter (approx) paellera 
- 1x  http://www.leroymerlin.es/fp/13115235/cartelas-sistema-sencillo-10-cartelas-sencillo
- 3x http://www.leroymerlin.es/fp/16142910/cremallera-sistema-sencillo-cremallera-sencillo-blanca
- 2x steel handles 
- 1x analog thermometer (0-600Cel.)
- Heat-resistant paint: http://www.leroymerlin.es/fp/298473/esmalte-anticalorico-titan-anticalorico-negro
- 2-3x 45-50 cm diameter circular grill trays

When I picked up the barrel it still had some residue of the previous contents, so I did about 5 rounds of washing it out with ample soap and water. I then let it dry, and after making sure there were no flammable vapors remaining in the barrel, I cut off the lid with an angle grinder. Keep the lid if you want to use it as a heat/smoke distibution plate; you can drill a bunch of 1" holes to let the air flow through it better. 

I drilled the three holes for the air intakes about 2" from the base of the barrel (120 degrees apart), and three more for vents near the top. I filled the barrel with some clean pallet wood, used an extractor fan to blow air into the intakes at the base, and burned wood until the barrel glowed red hot for 15~25 minutes. This may not actually get rid of all of the leftover carcinogenic chemicals in the remaining residue and paint, but I felt that it was good enough. it took a lot of elbow grease to get the charred paint off of the outside of the barrel! I used a steel wire brush and it took me ~3 hours. I drilled the remaining holes to mount the interior rack system, the handles, the temperature probes, etc. After cleaning the surface, I used a heat-resistant paint to coat the outside of the barrel. I did another few burns (at a lower temperature) to wear it in a bit, oiled up the inside, and started smoking!

### Materials for the coal basket:
- 1x expanded steel to form basket: http://www.leroymerlin.es/fp/13850305/chapa-de-acero-bruto-malla-mediano?pathFamilaFicha=420504
- 1x 35cm circular grill  for base of basket
- 2-3m stainless steel wire

I stitched together the basket with the expanded steel using the stainless steel wire, taking care to not shred my hands-- thick leather gloves are a must. I plan to build a bigger/stronger coal basket with thicker expanded steel & a welder.





