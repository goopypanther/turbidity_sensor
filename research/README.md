Research
========

Research materials and notes go here.

Turbidity
---------

Particles both scatter and absorb light, scattered light may be a better indicator of clarity than absorbed light because of translucent particles.

Research suggests infrared light is ideal for its indifference to the color of particular organic particles. 940nm (IR) LEDs and photodiodes are readily available. 850nm (closer to NIR) are also an option.

Biofouling
----------

Research suggests ultraviolet light can reduce the amount of biological growth on sensor surfaces. UVC will kill everything from barnacles to biofilms ([1](https://www.ncbi.nlm.nih.gov/pubmed/20024789), [2](https://www.oceannews.com/feature-story/2014/03/04/february-uv-irradiation-a-new-kind-of-antifoulant)) but LEDs are very expensive (>$100 each). Cheap UVA LEDs may provide some protection ([1](http://onlinelibrary.wiley.com/doi/10.1111/j.1365-2672.2010.04850.x/full)) but other studies seem to indicate that some species respond favorably to it ([1](http://plankt.oxfordjournals.org/content/16/12/1645.short), [2](https://www.ncbi.nlm.nih.gov/pubmed/17039372)), though this might differ between soil/freshwater/marine environments.

Measurement & Conversion
------------------------

Some possible discussed architectures:

 * Direct measurement of photodiodes
 * Transimpedence amplifier -> ADC
 * Closed loop LED intensity/transimpedence -> ADC
  * Automatic gain control

Other ideas include:

 * Dark current subtraction on each measurement
 * Pulse/frequency coding LED flashes for noise immunity
 * Temperature compensation on photodiodes
 * Differential sensing at 2 different distances/difference amplifier
  * Corrects for ambient light and temp effects

ADC
---

Internal microcontroller ADC may be of lower quality than desired. External chip option is strong.

Jeremy: I'm tempted by the kinetis M series microcontrollers that have 24-bit delta/sigma ADCs.

Sensor Communications
---------------------

Need robust communication bus between sensors at different depths. RS485 is a good contender.

Shore Communications
--------------------

Possibilities:

 * WiFi link to nearby shore internet
  * Super simple, some dive sites have wifi available from nearby venues
 * LTE/GSM radiomodem
  * Works for remote sites
 * Zigbee/802.15.4/nrf24 based radio link to internet connected shore station
  * Unlikely to be better than radiomodem solution

Enclosures & Waterproofing
--------------------------

Ideas:

 * Inductive charge/data with fully encapsulated modules
 * Modules in watertight
