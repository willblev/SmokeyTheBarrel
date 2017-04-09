# UDS_ATC
Automatic temperature controller (ATC) for an ugly drum smoker (UDS)

This is an automated smoker (controllable via the Blynk smartphone app) which uses an ESP8266 to measure 5 k-type thermocouple temperature probes, and controls a 12v DC blower fan, thereby regulating the temperature.

I cut off the lid, cleaned out, stripped paint, and re-painted a steel drum that previously contained motor oil. I used three brass 3/4'' pipe fittings as air intakes on the bottom and 3 more as vents on the top. Bought a large paellera to use as a new lid. Added handles and a modular rack system to adjust the height of the grills. Soon I will add an automated temperature control system using the microcontroller ESP8266 + 5x K-type thermocouples + 12V DC blower attached to one of the bottom air intakes.

See some images of the project [here](https://trello.com/c/GKH84JZ9/7-uds-ugly-drum-smoker-200l-steel-barrel-bbq-smoker)
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

### Materials for the coal basket:
- 1x expanded steel to form basket: http://www.leroymerlin.es/fp/13850305/chapa-de-acero-bruto-malla-mediano?pathFamilaFicha=420504
- 1x 35cm circular grill  for base of basket
- stainless steel wire

### Materials for automatic temperature controller:
- 1x ESP8266 12E module (I used the WeMos D1 mini)
- 5x K type thermocouples & amplifier circuits http://www.ebay.com/itm/181440455042?_trksid=p2060353.m2749.l2649&ssPageName
- 1x 12V DC blower fan with PWM speed control (4 wires)
- 1x 12V power supply
- 1x 12V -> 3.3V DC-DC step down power regulator
- 1x waterproof project box
