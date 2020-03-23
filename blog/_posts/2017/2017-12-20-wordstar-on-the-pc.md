---
layout: post
title: WordStar On The PC
date: 2017-12-20 10:00:00
permalink: /blog/2017/12/20/
machines:
  - id: ibm5150
    type: pcx86
    config: /configs/pcx86/xml/machine/5150/mda/256kb/machine.xml
    autoMount:
      A:
        name: PC DOS 2.00 (Disk 1)
      B:
        name: WordStar 3.24
    autoType: $date\r$time\rB:\rWS\r
  - id: scrollLEDs
    type: leds
    name: LED Scroller
    config: /devices/leds/scroller/ATT4425.json
styles:
  _scrollLEDs:
    position: relative;
    display: inline-block;
    float: left;
    margin-right: 32px;
    margin-bottom: 16px;
  _displayScroll:
    position: relative;
---

I recently added another disk to the PCjs Archives, [WordStar 3.24](/disks/pcx86/apps/other/wordstar/3.24/), along with a copy
of the article "[WordStar 3.24 and 3.3: MicroPro Does It Again... And Again](/disks/pcx86/apps/other/wordstar/#pc-magazine-review)",
an interesting review/rant from 1983 on this and other versions of WordStar for the IBM PC.

This is the earliest PC version of WordStar I've been able to locate so far.  Until now, the earliest version online was
[WordStar 3.30](/disks/pcx86/apps/other/wordstar/3.30/).  Sadly, the legendary *first* PC version, WordStar 3.02M, remains
elusive.

And, since this may be my last blog post of the year, here's a little scrolling LED display to wish everyone a happy new year.

{% include machine.html id="scrollLEDs" config="json" %}

<div id="scrollLEDs"><div id="displayScroll"></div></div>

The [LED Scroller](/devices/leds/scroller/) is built with a new set of [PCjs Devices](/modules/devices/) used in PCjs machines
such as:

* Texas Instruments [TI-42](/devices/ti42/machine/), [TI-55](/devices/ti55/machine/), and [TI-57](/devices/ti57/machine/rev0/) Programmable Calculators
* [John Conway's](http://www.conwaylife.com/wiki/John_Horton_Conway) "[Game of Life](http://www.conwaylife.com/wiki/Conway%27s_Game_of_Life)" Cellular Automaton built as an [LED Simulation](/devices/leds/life/)
* [Hasbro's](https://en.wikipedia.org/wiki/Hasbro) "[Lite-Brite](https://en.wikipedia.org/wiki/Lite-Brite)" reimagined as an animated [LED Simulation](/machines/led/lite-brite/)

The [LED Device](/modules/devices/led.js), in conjunction with the [LED Controller](/modules/devices/ledctrl.js), provides
a variety of LED types, layouts, and features, including built-in support for the 7-segment LED digits used in all the
TI Programmable Calculator displays.

{% include machine.html id="ibm5150" %}