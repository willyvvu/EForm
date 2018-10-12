# E-Form

The MIDI controller mediates between two vastly different worlds: the musician and computer. The hardware should capture the lightest touch yet accomodate the longest road trip. The interaction design should be musically intuitive for beginners yet efficient and usable on-stage for experts. The software must accomodate the fastest stacatto while rejecting noise in real-time. Form factor, weight, power draw, and sensor resolution all lay in delicate balance.

E-Form is an expressive multitouch music controller, sensitive to x/y position as well as pressure on its smooth surface. It takes a more evolved approach than the [MIDI controller](https://github.com/willy-vvu/Mixer) I built last year, putting emphasis on the multidisciplinary design across hardware and software.

![](EForm1.jpg)

![](EForm2.jpg)

![](EForm3.jpg)

![](EForm4.jpg)

![](EFormLive1.jpg)

![](EFormLive2.jpg)

![](EFormLive3.jpg)

![](EFormLive5.jpg)

![](EFormLive4.jpg)

---

## Behind the Scenes

Designing and building a performant, robust, MIDI spec-compliant, thin & light product is quite difficult, often requiring custom/homemade tools and components. Below are a few images showing some of the software and hardware processes used in construction.

![](EForm6.jpg)
*The pressure sensing layer: a grid of conductive foil and Velostat.*

![](EForm5.jpg)
*A visualation of my hand on the surface.*

The raw data from the sensing layer is quite a firehose when trying to visualize in real-time. Fortunately, I wrote an interactive Processing sketch to plot the pressure on each grid intersection right as it came off the microcontroller, which was immensely helpful for diagnosing the inevitable noise/wiring issues.

![](EForm7.jpg)
*Exposed wiring and homemade PCBs.*

![](EForm8.jpg)
*Software I made to edit and program the interface layout.*

Mapping pads to MIDI CC values in code was not a task I was willing to do by hand in code. Fortunately, I wrote a quick tool with an interface that allowed me to specify which regions of the controller corresponded to which MIDI messages. This mapping was then converted into lightly optimized C code which ran directly on the microcontroller.

### Specs

Dimensions: 300mm x 300mm x 12mm

Weight: About 500g

Touch Area: Edge-to-edge 300mm x 300mm

Touch Points: 1024

Touch Resolution: Sub-millimeter (computed)

Pressure Resolution: 1024 levels

Sample Rate: More than 60Hz

Haptics: Linear Resonant Actuator

Material cost: Less than $100

---

Supported by: [Council for the Arts at MIT](http://arts.mit.edu/welcome/camit/)

Learning Focus: PCB Design, PCB Milling, Vinyl Cutting, Surface Mount Soldering, Product Design, Integrated Circuits, Sensing Grids, Performance Interfaces, Music Production, Metaprogramming

Media: MIDI Controller, Physical Interface, Icon Design, Object

Software: C++, JavaScript, p5.js, Processing, Inkscape, Bitwig Studio, Fab Modules

Hardware: PCB Mill, Vinyl Cutter, Soldering Iron, Bandsaw, Teensy

Date: June 2017
