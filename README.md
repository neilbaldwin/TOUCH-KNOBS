# TOUCH-KNOBS
Custom modular-style knobs for Touch OSC

## What is TOUCH-KNOBS?

Born partly out of the desire to have a knob-type object that was simultaneously simpler and more customizable than the stock Radial or Encoder Touch OSC objects, and partly because I got a tiny-bit obsessed with inventing a way to customise objects at run-time.

TOUCH-KNOBS uses a simple and readable parameter string placed in the Tag parameter of the Knob object (actually a group of related components that fit together to make the Knob) that allows you to customise the Knob. You can customise:

* knob color
* pointer color
* pointer size
* pointer offset (from edge of knob)
* three 'styles': "flat", "short" and "tall" (the last two have a pseudo 3D effect)
* knob outline (on/off and color)
* drop shadow on/off

In addition, the geometry of the Knob (and it's sub-components) is all re-calculated at run-time based on the dimensions of the Knob object (Group). You *turn* the Knob by touch-dragging up and down rather than the rotational gesture required by the Radial and Encoder objects.

## How do I use it?

Download the TOUCH-KNOBS.tosc file and open it in Touch OSC. You will see a bunch of TOUCH-KNOBS to play with. We'll get to the customisation and options but first you need to know the fundamentals.

### TOUCH-KNOB Components

There are two *components* to TOUCH-KNOBS:

#### Root Lua Script

This script does 95% of the work. It's mainly concerned with parsing the Knob parameters and setting up the geometry, colors and options. It also contains a table of CSS Color Names as when specifying colors in your Knob you can use either the CSS name or a hex string in the format `0xRRGGBB`

If you want to use TOUCH-KNOBS in your project, this Lua script need to go in the document root of your Touch OSC file.

#### "Knob" Objects

Knob objects are actually Group objects containing the various components that make up the Knob geometry: BODY, POINTER, SHADOW1, SHADOW2, OUTLINE, FADER and DROP_SHADOW (more on these later).

The creation/customisation parameters go in the Tag parameter of the Knob (Group).

To make a new Knob just copy-and-paste and existing one then change it's parameters in the Tag.

> [!NOTE]
> A note

