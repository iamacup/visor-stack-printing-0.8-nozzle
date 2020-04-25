## 0.8 Nozzle PLA Visor Stacks in PrusaSlicer

these are PrusaSlicer setups for 0.8 nozzles using the [Hack The Pandemic](www.hackthepandemic.co.uk) visor, which is based off of the N3DPS model 3.6 but with smoother tool paths for 100% perimeter prints, you can use other nozzle sizes for this but you will need to adjust the space between the models manually.

**Depending on your printer, these will print between 18.4 mins and 24.5 mins per visor**

| Type | 15x Print Time | 30x Print Time |
| ------- | ------ | ------ |
| Type 1 | 6h 8m | 12h 14m |
| Type 2 | 5h 22m | 10h 43m |
| Type 3 | 4h 55m | 9h 48m |
| Type 4 | 4h 37m | 9h 12m |

I did a lot of experimentation with the 0.8 nozzle on both PETG and PLA – it is very hard to get PETG to work because of how sticky it is compared to PLA so this repo is for PLA only.

<blockquote class="imgur-embed-pub" lang="en" data-id="a/CgnUVlC" data-context="false" ><a href="//imgur.com/a/CgnUVlC"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>

## How This Works

We need the top layer of every visor to be as good as possible so it can serve as a nice flat base for the next visor so we:

* Slow down `top layers` of a visor
* Slow down the `bottom layer` of a visor
* Slow down the `bottom layer + 1` of a visor

We need the bottom layer of a visor to 'stay together' and not stick to the visor below it, especially considering there is an air gap - so we:

* Make the `bottom layer + 1` of a visor smaller to act like a 'first layer' and make sure we minimise delamination of the `bottom layer`


<PICTURE ABOUT SETUP OF FIRST LAYER>

| Print Speeds | Layer Heights |
| ------- | ------ |
| ![img]() | ![img]() |


## Testing

There are TEST project files that are a simple 3 stack for test runs


## Changing The Printer

The PrusaSlicer project files in this repo are setup for **MK3S MMU2S** to print from the filament in slot 3, you will need to change the printer to whatever you have, be it Prusa or not. 

1. Change the **Printer**
2. Update the Nozzle Diameter and Layer Height Limit Max in the *Printer Settings* as shown below:

<img here> 

3. Make sure the *Print Settings* and *Filament* are unchanged


## General Print Settings

| Temp | Value | Notes |
| ------- | ------ | ------ |
| Temp | 130 | Temp is this high as there was lots of layer delamination, feel free to tweak based on your filament |
| Material | PLA |  |
| Air Gap | 0.35 | Tested between 0.1 and 0.5, 0.35 seemed to work best |



## Project Files

| Property | 'slow' Layer Speeds | Files |
| ------- | ------ | <link> |
| Type 1 | 15 | <link> |
| Type 2 | 20 | <link> |
| Type 3 | 25 | <link> |
| Type 4 | 30 | <link> |

