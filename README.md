## Purpose

This was developed to automate watering plants with gravity using a WiFi connected power outlet. A water reservoir is placed at a greater height than the outputs and a normally closed, on/off solenoid valve controls water flowing downward due to gravity. It can easily be built with items bought at a hardware store or online. While this design has 10 outputs it can easily be modified for more or less.

## The design

While I use a Wemo in this, any IOT power socket will work interchangeably with this design. It is used to turn the power on and off in the circuit. The Wemo smart outlet has the capability of being switched on and off both locally and remotely. Due to 1 minute being the smallest increment of control available on the wemo, we will have to create another way to de-energize and close the N/C (normally closed) valve faster. For this I used a time delay relay. 

Note: If there is an IOT socket on the market that can reliably turn on and off the power in smaller time increments than one minute, the delay-on relay could be taken out of the design, however I am not aware of one available.

![design](https://dl.dropboxusercontent.com/s/yewsusirbce8ia5/design.png)

First the wemo switch will turn on. This will energize the valve and open it, allowing the water to flow. When the wemo is turned on, the delay-on relay timer will begin its countdown. After the set time is reached, the N/C circuit on the relay will open and the the N/O (normally open) circuit will close. Since the valve is wired on the N/C circuit, the valve will de-energize and close after the time runs out.

Basically, turn wemo on then valve opens and water flows. After the set time runs out, relay turns off valve.

There are 3 main parts:

- The water reservoir
- The valve/relay assembly
- the outputs

If we set the timer to 10 seconds moving from left to right. (before the wemo is turned on and after the wemo is turned off)


| ----------- | Time Off| Time 0 | Time 10 | Time 60 |
| ----------- | ------- | ------ | ------- | ------- |
| Wemo        | Off     |  On    |  On     |  Off    |
| Valve       | Closed  | Open   | Closed  | Closed  |
| Relay timer | Off     | Start  | Stop    | Off     |
| N/C Circuit | Closed  | Closed | Open    | Closed  |
| N/O Circuit | Open    | Open   | Closed  | Open    |

## Final result

![Image of reservoir and valve](https://dl.dropboxusercontent.com/s/el61ygrr2me428m/20180118_152428.jpg)
![Image of output](https://dl.dropboxusercontent.com/s/6v5zico94f435j6/Output.jpg)
This is the final Assembly. It has 10 outputs in series and a 1 gallon reservoir placed about 4 feet above the plants on a shelf.
![Image of outputs](https://dl.dropboxusercontent.com/s/w6eepkhk5qq6sqw/20180122_090435.jpg)

### Materials I used

[1x 10’ length 3/8" ID , 1/2" OD clear PVC tubing](https://www.amazon.com/gp/product/B000HE5DUQ/ref=oh_aui_detailpage_o00_s00?ie=UTF8&psc=1)

[10x 3 way tees](https://www.amazon.com/gp/product/B017UXJQYA/ref=oh_aui_detailpage_o03_s00?ie=UTF8&psc=1)

[12x plastic caps for reducers](https://www.amazon.com/gp/product/B01MTLEK7F/ref=oh_aui_detailpage_o09_s00?ie=UTF8&psc=1)

[1x On/off  N/C solenoid valve](https://www.amazon.com/gp/product/B016YO73E6/ref=oh_aui_detailpage_o02_s00?ie=UTF8&psc=1)

[2x 1/2" NPT to 3/8" barb](https://www.amazon.com/gp/product/B003RVV6IO/ref=oh_aui_detailpage_o08_s00?ie=UTF8&psc=1)

[1x roll Teflon PTFE thread tape](https://www.amazon.com/Teflon-Thread-Seal-Tape-Sealing/dp/B06WW6M7F9/ref=sr_1_1_sspa?s=industrial&ie=UTF8&qid=1516587138&sr=1-1-spons&keywords=teflon+tape&psc=1)

[1x N/c  & N/O relay switch](https://www.amazon.com/gp/product/B00VG9J6SQ/ref=oh_aui_detailpage_o05_s00?ie=UTF8&psc=1)

[1x 10’ Lamp wire](https://www.amazon.com/gp/product/B015YFAPAA/ref=oh_aui_detailpage_o06_s00?ie=UTF8&psc=1)

[1x Electric project box](https://www.amazon.com/gp/product/B0714N2737/ref=oh_aui_detailpage_o08_s00?ie=UTF8&psc=1)

[2x PG7 Cable glands](https://www.amazon.com/gp/product/B06VSSX599/ref=oh_aui_detailpage_o07_s00?ie=UTF8&psc=1)

[1x 3/8" OD Spigot](https://www.amazon.com/gp/product/B01BWMR49E/ref=oh_aui_detailpage_o07_s00?ie=UTF8&psc=1)

[1x wemo smart socket](https://www.amazon.com/Smart-Enabled-Amazon-Google-Assistant/dp/B01NBI0A6R/ref=sr_1_4?s=hi&ie=UTF8&qid=1516587200&sr=1-4&keywords=wemo+smart+socket)

[Hose clamps](https://www.amazon.com/Adjustable-Stainless-Steel-Clamps-9-16mm/dp/B075HVFTM1/ref=sr_1_11?s=hi&ie=UTF8&qid=1516587228&sr=1-11&keywords=hose+clamps+3%2F8+inch)

[1/2" hose mount brackets](https://www.amazon.com/gp/product/B002TIFVWI/ref=oh_aui_detailpage_o05_s00?ie=UTF8&psc=1)

[1/2" Phillips head screws](https://www.amazon.com/gp/product/B01MFAIS08/ref=oh_aui_detailpage_o05_s00?ie=UTF8&psc=1)

[Quick connect couplings one side](https://www.amazon.com/gp/product/B003M07S46/ref=oh_aui_detailpage_o06_s00?ie=UTF8&psc=1)

[Quick connect coupling other side](https://www.amazon.com/gp/product/B003M03VOC/ref=oh_aui_detailpage_o06_s00?ie=UTF8&psc=1)

[Water container](https://www.amazon.com/Gallon-Plastic-Shatter-Proof-Container-Storage/dp/B071WT6WG4/ref=sr_1_10_sspa?s=home-garden&ie=UTF8&qid=1516587392&sr=1-10-spons&keywords=1+gallon+water+container+spigot&psc=1)

[Wooden skewers](https://www.amazon.com/Farberware-Bamboo-Skewers-12-Inch-Natural/dp/B005D6GCSA/ref=sr_1_4?ie=UTF8&qid=1516587345&sr=8-4&keywords=wooden+skewers)

[Loctite plastic](https://www.amazon.com/Loctite-Plastics-Bonding-Activator-681925/dp/B000Y3LHXW/ref=sr_1_1?ie=UTF8&qid=1516630081&sr=8-1&keywords=loctite+plastic)

[JB water weld](https://www.amazon.com/J-B-Weld-JB-8277-Waterweld/dp/B00SPNR8X6/ref=sr_1_2?s=hi&ie=UTF8&qid=1516630119&sr=1-2&keywords=jb+weld+water)


### Tools

- Electric drill

- 7/8" wrench

- Heat gun / hair dryer

- Phillips head Screw driver

- Flat head screw driver

## Main steps to build one yourself

### Build water reservoir

- Connect the spigot to the water container and seal it using JB Weld
![reservoir](https://dl.dropboxusercontent.com/s/z36bwj65y41oq7j/20180115_135329.jpg)
- When the sealant is all dry, heat up the end of the PVC tubing and get it soft so it is easy to slide onto the barb on the spigot. Tighten a clamp onto that. Do the same thing for the couplings.
![reservoir](https://dl.dropboxusercontent.com/s/f9jt5s4p0g2aua0/20180116_173802.jpg)

### Assemble delay relay and box

- Wire the relay to a power outlet. Drill two holes on each side of the power box and connect the wire glands. Place the relay into the box and run the wire to the valve out one side and the wire to the power socket out another.

![circuit](https://dl.dropboxusercontent.com/s/145bkkecxttzkf8/circuit.png)

![relay in box](https://dl.dropboxusercontent.com/s/9qmpy5jma7v59ge/20180115_170421.jpg)


### Connect relay and valve

- Unscrew and pop off the plastic piece on the top of the valve

![valve and relay](https://dl.dropboxusercontent.com/s/ooonwq56kyw6a37/20180118_142048.jpg)

- Run the wire through the plastic opening
![valve and relay 2](https://dl.dropboxusercontent.com/s/9icf7uzz4dysgdg/20180118_141807.jpg)

- Wire into the terminals on the left and right

![valve and relay 3](https://dl.dropboxusercontent.com/s/ib51munm7mltxmb/20180118_141929.jpg)

### Assemble water outputs

- Measure from the center of each plant and ensure each output is spread out at the proper interval. You can use JB weld to ensure that the connections are sealed and won't leak.

- Cutting off the tips of the bottle caps make good reducers to control the output depending on your application. Use loctite or jb weld to fit them to the 3 way tee outputs.

![outputs](https://dl.dropboxusercontent.com/s/3yltzgamlgbqzvv/20180115_163712.jpg)
![outputs all](https://dl.dropboxusercontent.com/s/uptzwt5fbdhdxlw/20180114_111429.jpg)

### Connect Everything Together

- Connect the couplings together
- wrap teflon tape around the threads of the 1/2" NPT to 3/8" barb connections. Fit them to the valves and tighten with a 7/8" wrench and make sure they seal well. connect the tubing and tighten with hose clamps.
![Valve](https://dl.dropboxusercontent.com/s/gu32mphbz5hd249/20180118_140807.jpg)
- Ensure all hose clamps are tight and there is no leaks.

### Test and Use

Disconnect the water reservoir assembly using the quick disconnect. Fill the water reservior with water and reconnect back inline. Press the button on the wemo switch or inside the wemo app. If you have a home AI assistant like Alexa you can program it to turn on using voice. The valve will open and then close in the set time. Make sure to add a rule on your wemo app that tells the wemo switch to automatically turn off after 1 minute whenever the switch is turned on. Additionally you can now put the plants on a watering schedule.
