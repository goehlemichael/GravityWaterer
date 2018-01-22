## Water your plants from anywhere

This was developed to automate the watering of plants with gravity. A normally closed, on/off solenoid valve controls water flow due to gravity. It can be easily built with items bought at a hardware store or online.

## The design

The Wemo smart outlet has the capability of being switched on and off both localy and remotely. Due to 1 minute being the smallest increment we will have to create another way to denergize and close the N/C valve.

First the wemo switch will turn on. This will energize the valve opening it and allowing the water to flow. At the same time the wemo is turned on the delay on relay timer will begin. After the set time the N/C circuit on the relay will open and the the N/O circuit will close. With the valve on the N/C circuit, the valve will de-energize and close. Using a wemo rule that tells the wemo to always shut off after a minute whenever it turns on causes the wemo to also power down after a minute. Thus restarting the cycle.

Basically when the wemo device is turned on the valve opens allowing the water to flow and water the plants. Then after the set time runs out, a relay turns off the valve by cutting its power.

There are 3 main parts:

- The water reservior
- The valve/relay assembly
- the outputs

So assuming we set the timer to 10 seconds moving from left to right. (before the wemo is turned on and after the wemo is turned off)


| ----------- | Time Off| Time 0 | Time 10 | Time 60 |
| ----------- | ------- | ------ | ------- | ------- |
| Wemo        | Off     |  On    |  On     |  Off    |
| Valve       | Closed  | Open   | Closed  | Closed  |
| relay timer | Off     | Start  | Stop    | Off     |
| N/C Circuit | Closed  | Closed | Open    | Closed  |
| N/O Circuit | Open    | Open   | Closed  | Open    |

## Final Result

![Image of reservior and valve](https://dl.dropboxusercontent.com/s/el61ygrr2me428m/20180118_152428.jpg)
![Image of output](https://dl.dropboxusercontent.com/s/6v5zico94f435j6/Output.jpg)
This is the final product. This one has 10 outputs in series and a 1 gallon reservior fixed about 4 feet above the plants on a shelf. 

### Materials (note I'm linking to specific items to reduce ambiguity, you can use whatever materials you would like)

[1x 10’ length 3/8" ID , 1/2" OD clear PVC tubing](https://www.amazon.com/gp/product/B000HE5DUQ/ref=oh_aui_detailpage_o00_s00?ie=UTF8&psc=1)

[10x 3 way tees](https://www.amazon.com/gp/product/B017UXJQYA/ref=oh_aui_detailpage_o03_s00?ie=UTF8&psc=1)

[12x plastic caps for reducers](https://www.amazon.com/gp/product/B01MTLEK7F/ref=oh_aui_detailpage_o09_s00?ie=UTF8&psc=1)

[1x On/off  N/C solenoid valve](https://www.amazon.com/gp/product/B016YO73E6/ref=oh_aui_detailpage_o02_s00?ie=UTF8&psc=1)

[2x 1/2" NPT to 3/8" barb](https://www.amazon.com/gp/product/B003RVV6IO/ref=oh_aui_detailpage_o08_s00?ie=UTF8&psc=1)

[1x roll Teflon PTFE thread tape](https://www.amazon.com/Teflon-Thread-Seal-Tape-Sealing/dp/B06WW6M7F9/ref=sr_1_1_sspa?s=industrial&ie=UTF8&qid=1516587138&sr=1-1-spons&keywords=teflon+tape&psc=1)

[1x N/c  & N/o relay switch](https://www.amazon.com/gp/product/B00VG9J6SQ/ref=oh_aui_detailpage_o05_s00?ie=UTF8&psc=1)

[1x 10’ Lamp wire](https://www.amazon.com/gp/product/B015YFAPAA/ref=oh_aui_detailpage_o06_s00?ie=UTF8&psc=1)

[1x Electric project box](https://www.amazon.com/gp/product/B0714N2737/ref=oh_aui_detailpage_o08_s00?ie=UTF8&psc=1)

[2x Cable glands](https://www.amazon.com/gp/product/B06VSSX599/ref=oh_aui_detailpage_o07_s00?ie=UTF8&psc=1)

[1x 3/8" OD Spigot](https://www.amazon.com/gp/product/B01BWMR49E/ref=oh_aui_detailpage_o07_s00?ie=UTF8&psc=1)

[1x wemo smart socket](https://www.amazon.com/Smart-Enabled-Amazon-Google-Assistant/dp/B01NBI0A6R/ref=sr_1_4?s=hi&ie=UTF8&qid=1516587200&sr=1-4&keywords=wemo+smart+socket)

[7x Hose clamps](https://www.amazon.com/Adjustable-Stainless-Steel-Clamps-9-16mm/dp/B075HVFTM1/ref=sr_1_11?s=hi&ie=UTF8&qid=1516587228&sr=1-11&keywords=hose+clamps+3%2F8+inch)

[C clamp 1/2" hose mount brackets](https://www.amazon.com/gp/product/B002TIFVWI/ref=oh_aui_detailpage_o05_s00?ie=UTF8&psc=1)

[1/2" Phillips head screws](https://www.amazon.com/gp/product/B01MFAIS08/ref=oh_aui_detailpage_o05_s00?ie=UTF8&psc=1)

[Quick connect couplings one side]](https://www.amazon.com/gp/product/B003M07S46/ref=oh_aui_detailpage_o06_s00?ie=UTF8&psc=1)

[quick connect coupling other side](https://www.amazon.com/gp/product/B003M03VOC/ref=oh_aui_detailpage_o06_s00?ie=UTF8&psc=1)

[Water container](1 gallon ideally with pre-cut 1" diameter hole for spigot)] (https://www.amazon.com/Gallon-Plastic-Shatter-Proof-Container-Storage/dp/B071WT6WG4/ref=sr_1_10_sspa?s=home-garden&ie=UTF8&qid=1516587392&sr=1-10-spons&keywords=1+gallon+water+container+spigot&psc=1)

[Wooden skewers (holds outputs up)](https://www.amazon.com/Farberware-Bamboo-Skewers-12-Inch-Natural/dp/B005D6GCSA/ref=sr_1_4?ie=UTF8&qid=1516587345&sr=8-4&keywords=wooden+skewers)


### Tools

- Electric drill

- 7/8" wrench

- Heat gun / hair dryer

- Phillips head Screw driver

- Flat head screw driver

- Loctite (optional)

- JB Weld water weld 

## Main steps to build one yourself

### Build water reservior

1. Connect the Spigot to the water container and seal it up using JB Weld
![reservior](https://dl.dropboxusercontent.com/s/z36bwj65y41oq7j/20180115_135329.jpg)
2. When its all dry heat up the end of the PVC tubing to get it soft and slide it onto the barb on the spigot. Tighten a clamp onto it. Do the same thing for the couplings.
![reservior](https://dl.dropboxusercontent.com/s/mzp74xfjtlu4z8t/20180116_170207.jpg)

### Assemble delay relay and electric box

1. Wire the relay to a power outlet. If you do not know what you are doing with wiring find someone who does or find some help online. drill two holes on each side of the power box and connect the wire glands. Place the relay into the box and run the wire to the valve out one side and the wire to the power socket out another.

![circuit](https://dl.dropboxusercontent.com/s/145bkkecxttzkf8/circuit.png)

![relay in box](https://dl.dropboxusercontent.com/s/9qmpy5jma7v59ge/20180115_170421.jpg)


### Connect relay and valve

1. There will only be two wires to connect to the valve. It requires disasemblying the top assembly on the valve and running the wire into the connection assembly.

![valve and relay](https://dl.dropboxusercontent.com/s/ooonwq56kyw6a37/20180118_142048.jpg)
![valve and relay 2](https://dl.dropboxusercontent.com/s/9icf7uzz4dysgdg/20180118_141807.jpg)
![valve and relay 3](https://dl.dropboxusercontent.com/s/ib51munm7mltxmb/20180118_141929.jpg)

### Assemble outputs

1. Measure out and ensure that each output is spread out at the proper interval. You can use JB weld to ensure that the connections are sealed and won't leak.

![outputs](https://dl.dropboxusercontent.com/s/3yltzgamlgbqzvv/20180115_163712.jpg)
![outputs all](https://dl.dropboxusercontent.com/s/uptzwt5fbdhdxlw/20180114_111429.jpg)

### Connect Everything Together

1. Connect the couplings together
2. wrap teflon tape around the threads of the 1/2" NPT to 3/8" barb connections. Fit them to the valves and tighten with a 7/8" wrench and make sure they seal well. connect the tubing and tighten the tubing with hose clamps.
3. Ensure all hose clamps are tight and there is no leaks.

### Test and Use

Disconnect the water reservior assembly using the quick disconnect. Fill the water reservior with water and then press the button on the wemo switch or inside the wemo app. If you have a home AI assistant like Alexa you can program it to turn on using voice. The valve will open and then close in the set time. Make sure to set a rule on your wemo app that tells the wemo switch to automatically turn off after a minute whenver the switch is turned on.
