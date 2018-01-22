## Water your plants from anywhere

This was developed to automate the watering of plants with gravity. This design utilizes an on/off solenoid valve to control the flow of water being powered by gravity.

This setup is ideal for windows or small areas where indoor plants are located and need to be watered frequently. The water reservoir needs to be located higher than the outputs.

## Reasoning for design

The Wemo smart outlet has the capability of being switched on and off both localy and remotely. Due to 1 minute being the smallest increment we will have to create another way to denergize and close the N/C valve.

First the wemo switch will turn on. This will energize the valve opening it and allowing the water to flow. At the same time the wemo is turned on the delay on relay timer will begin. After the set time the N/C circuit on the relay will open and the the N/O circuit will close. With the valve on the N/C circuit, the valve will de-energize and close. Using a wemo rule that tells the wemo to always shut off after a minute whenever it turns on causes the wemo to also power down after a minute. Thus restarting the cycle.

Basically when the wemo device is turned on the valve opens allowing the water to flow and water the plants.

There are 3 main parts:

- The water reservior
- The valve/relay assembly
- the outputs

So assuming we set the timer to 10 seconds moving from left to right. (before the wemo is turned on and after the wemo is turned off)


| ----------- | Time Off| Time 0 | Time 10 | Time 60 |
| ----------- | ------- | ------ | ------- | ------- |
| Wemo        | Off     |  On    |  On     |  Off    |
| Valve       | Closed  | Open   | Closed  | Closed  |
| relay timer | Off     | Start  | Stop    | Off     |
| N/C Circuit | Closed  | Closed | Open    | Closed  |
| N/O Circuit | Open    | Open   | Closed  | Open    |

## Final Result

![Image of reservior and valve](https://dl.dropboxusercontent.com/s/3bhcuvweozbe6vf/20180118_124644.jpg)
![Image of output](https://dl.dropboxusercontent.com/s/6v5zico94f435j6/Output.jpg)
This is the final product. This one has 10 outputs in series and a 1 gallon reservior fixed about 4 feet above the plants on a shelf. 

### Materials

- 1x 10’ length 3/8" ID , 1/2" OD clear PVC tubing

- 10x 3 way tees

- 1x On/off  N/C solenoid valve

- 2x 1/2" NPT to 3/8" barb

- 1x roll Teflon PTFE thread tape

- 1x N/c  & N/o relay switch

- 1x 10’ Lamp wire 

- 1x Electric project box

- 2x Cable glands

- 1x 3/8" OD Spigot

- 1x wemo smart socket

- 7x Hose clamps

- C clamp 1/2" hose mount brackets

- 1/2" Phillips head screws

- Quick connect couplings ( I used CPC quick disconnects)

- Water container ( 1 gallon ideally with pre-cut 1" diameter hole for spigot)

- Wooden skewers (holds outputs up)


### Tools

- Drill

- 7/8 wrench

- Heat gun / blow dryer

- Phillips head Screw driver

- Flat head screw driver

- loctite

- JB Weld water weld

## Main Steps

### Build Water reservior

### Assemble delay relay and electric box

### Assemble ouputs

### Connect Everything Together
