---
title: Display and Top Cover
date: 2025-09-24 21:00 -0500
tags: [cad, chassis, display]
media_subpath: /assets/2025-09-24-Display-and-Top-Cover/
---

### Welcome to the first real post in the ReFrame 18 devlog! This post details the design process of the top/display portion of the laptop. The current, mostly-complete iteration of the design is only 9.1mm thick!
![A CAD screenshot of the full top/display portion assembly.](Full-Assembly.png)
_The full top/display portion assembly._

## Selecting the Display
The first step in designing the ReFrame 18 was picking a display. I had a few requirements:
- 18"
- 2560x1600 (16:10, WQXGA)
- at least 144hz refresh rate
- 4-lane, 40-pin eDP connector on the back of the display
- Non touch screen, for eDP pinout compatibility

Take this with a grain of salt because I can't confirm it until I have hardware in hand, but from what I can tell, the Framework 16's display uses a standard eDP pinout; the Framework 16's eDP cable adapts the custom pinout on the mainboard's eDP connector to a standard 4-lane, 40-pin, non-touch-screen pinout on the display end, so I had to find a display that met these requirements and had its connector on the back, like the Framework 16's display does. To find the right display, I used [Panelook's](https://www.panelook.com/index.php) advanced search tool. Based on specs, availability and pricing, I landed on the [BOE NE180QDM-NZ2](https://www.panelook.com/NE180QDM-NZ2_BOE_18.0_LCM_overview_60286.html). This is a 240hz IPS panel that was used in the [2023 ASUS ROG Strix SCAR 18](https://rog.asus.com/laptops/rog-strix/rog-strix-scar-18-2023-series/). The one problem here is that this display's eDP connector has a 0.5mm pitch while the Framework 16's eDP cable has a 0.4mm pitch, but there are adapters available on sites like ebay.
![A screenshot of the display's Panelook product page.](Panelook.png)
_The display's Panelook product page._

## Top Cover CAD
To design the top cover in CAD, I first sketched the dimensions of the display and webcam module and extruded them to create placeholder shapes. Then, I sketched a larger rectangle around it; this larger rectangle would be the outer edge of the top cover and was sized to include a small gap around the sides of the display and webcam module, as well as some extra space at the bottom for the hinges and eDP cable. Some space was also left behind the display to make room for cables to be run behind it and for bracing to be added for rigidity.

I picked a largely arbitrary position for the hinges, as they can be moved later. The bolt pattern is that of the Framework 16 hinges, although I might end up using different hinges if the Framework ones aren't strong enough.
![A screenshot from a CAD program of the mounting point for the left hinge.](Hinge-Mount.png)
_The mounting point for the left hinge._

The minimum thickness of the top cover is 0.8mm, with bracing between the hinges and their opposite corners that adds an extra 0.4mm. 
![A top-down CAD screenshot of the top cover.](Top-Cover-Top-View.png)
_A top-down view of the top cover._

There are additional features extending further out from the inside of the top cover. The display will rest on these, attached with adhesive strips that can be removed with pull tabs. There are also four tabs with threaded holes (M2.5) for mounting the bezel.
![A CAD screenshot of one of the mounting points for the display.](Display-Mount.png)
_The left mounting point for the display, which will have an adhesive strip on it._
![A CAD screenshot of the center support for the display.](Center-Display-Support.png)
_The center support for the display._
![A CAD screenshot of one of the tabs and screw holes for mounting the bezel.](Bezel-Mount.png)
_The top left mounting point for the bezel._

The Framework 16 webcam module will be mounted with two M2.5 screws, and will sit on its own "platform" like the display does.
![A CAD screenshot of the webcam's mounting platform.](Webcam-Mount.png)
_The webcam module's mounting platform._

## Bezel CAD
The bezel will be 1.3mm thick ABS. It will have clearance holes, each countersunk, for its mounting screws. The bezel will also have a small, thin piece of polycarbonate inset into it to protect the webcam.
![A top-down CAD screenshot of the bezel.](Bezel-Top-View.png)
_A top-down view of the bezel._

## What's Next?
The CAD for the top cover is now mostly done. It may change slightly if my choice of hinge changes, and once the hinge position is finalized the bezel may be modified to suit. The next step of the project is to begin designing the bottom chassis, using the overall dimensions of the top cover and bezel assembly as a starting point. The first component of the bottom chassis to be designed will likely be the mechanical keyboard, as it'll be on top of the stack of components and will allow me to determine the overall thickness of the bottom cover. I'll be able to add all of the other components from there.
