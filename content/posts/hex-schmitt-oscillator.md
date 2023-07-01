---
title: "HEX oscillator"
date: 2023-07-01T19:38:00+02:00
tags: ["oscillator", "hex-inverter"]
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: false
disableHLJS: true # to disable highlightjs
disableShare: true
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
---

## Hex inverter oscillator

Today I dipped my toes into the world of analog synth and created my first oscillator.
I based my design on a hex schmitt-trigger inverter chip, more precise the CD40106BE.

I just picked up some components that I had laying around and created the following circuit:

![Electrical schematic of oscillator circuit](/images/hex-schmitt-oscillator/schematic.png)

This seemed to produce some decent frequency range that could be usable for music (130 Hz to ~3 kHz).

![Image of oscilloscope where oscillator generates 130 Hz signal](/images/hex-schmitt-oscillator/hex-osc-130-Hz.png)
![Image of oscilloscope where oscillator generates 3 kHz signal](/images/hex-schmitt-oscillator/hex-osc-3-kHz.png)

However when reaching the "end" of the potentiometer it seems like the capacitor is too large and makes the charge time long enough that the signal becomes a triangle wave instead of a square wave.

![Image of oscilloscope where oscillator generates 15 kHz signal](/images/hex-schmitt-oscillator/hex-osc-15-kHz.png)

I have not put this down on the math table yet so the 15 kHz probably correlates pretty well with the capacity of the capacitor I chose.

Since I haven't built a proper eurorack power supply I for now only have this 4V power supply that I used and I also don't have any way of playing this into a reasonable strength for headphones and/or sound interface so this small project was only for getting myself started in this.
I've just recently moved and I want to fix a proper workshop before I start doing some bigger project so I'll probably start with that before I continue with a power supply and end amplifier.
But I hope that I'll be writing more here soon.
