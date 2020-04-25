## 0.8 Nozzle PLA Visor Stacks in PrusaSlicer

**[Video of stack splitting](https://imgur.com/YbhcxAj)**

these are PrusaSlicer setups for 0.8 nozzles using the [Hack The Pandemic](www.hackthepandemic.co.uk) visor, which is based off of the N3DPS model 3.6 but with smoother tool paths for 100% perimeter prints, you can use other nozzle sizes for this but you will need to adjust the space between the models manually.

**Depending on your printer, these will print between 18.4 mins and 24.5 mins per visor**

| Type | 15x Print Time | 30x Print Time |
| ------- | ------ | ------ |
| Type 1 | 6h 8m | 12h 14m |
| Type 2 | 5h 22m | 10h 43m |
| Type 3 | 4h 55m | 9h 48m |
| Type 4 | 4h 37m | 9h 12m |

I did a lot of experimentation with the 0.8 nozzle on both PETG and PLA – it is very hard to get PETG to work because of how sticky it is compared to PLA so this repo is for PLA only.


## How This Works

We need the top layer of every visor to be as good as possible so it can serve as a nice flat base for the next visor so we:

* Slow down `top layers` of a visor

We also need the bottom layer to be consistent, but split off from the previous visor so we: 

* Slow down the `bottom layer` and `bottom layer + 1` of a visor
* Make the `bottom layer + 1` of a visor smaller to act like a 'first layer' and make sure we minimise delamination of the `bottom layer`

| Print Speeds | Layer Heights |
| ------- | ------ |
| ![img](https://github.com/iamacup/visor-stack-printing-0.8-nozzle/raw/master/files/images/layer-speeds.png) | ![img](https://github.com/iamacup/visor-stack-printing-0.8-nozzle/raw/master/files/images/layer-heights.png) |


## Project Files

There are TEST project files that are a 3 stack for each print type

| Name | 'slow' Layer Speeds | Files |
| ------- | ------ | ----- |
| Type 1 | 15 | [files/PrusaSlicer/1](https://github.com/iamacup/visor-stack-printing-0.8-nozzle/tree/master/files/PrusaSlicer/1) |
| Type 2 | 20 | [files/PrusaSlicer/2](https://github.com/iamacup/visor-stack-printing-0.8-nozzle/tree/master/files/PrusaSlicer/2) |
| Type 3 | 25 | [files/PrusaSlicer/3](https://github.com/iamacup/visor-stack-printing-0.8-nozzle/tree/master/files/PrusaSlicer/3) |
| Type 4 | 30 | [files/PrusaSlicer/4](https://github.com/iamacup/visor-stack-printing-0.8-nozzle/tree/master/files/PrusaSlicer/4) |


## General Print Settings

| Temp | Value | Notes |
| ------- | ------ | ------ |
| Temp | 130 | Temp is this high as there was lots of layer delamination, feel free to tweak based on your filament |
| Material | PLA |  |
| Air Gap | 0.35 | Tested between 0.1 and 0.5, 0.35 seemed to work best |


## Changing The Printer

The PrusaSlicer project files in this repo are setup for **MK3S MMU2S** to print from the filament in slot 3, you will need to change the printer to whatever you have, be it Prusa or not. 

1. Change the **Printer**
2. Update the Nozzle Diameter and Layer Height Limit Max in the *Printer Settings* as shown below:

![img](https://github.com/iamacup/visor-stack-printing-0.8-nozzle/raw/master/files/images/diff-printer.png)

3. Make sure the *Print Settings* and *Filament* are unchanged




