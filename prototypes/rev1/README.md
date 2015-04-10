This prototype is intended to test the behavior of IR LED/photodiode pairs at a variety of angles to narrow down the best method of obtaining measurements of water turbidity (direct opacity measurement/rayleigh scattering).

Each photodiode is connected to a transimpedance amplifier and broken out to a header for oscope/adc conversion. Everything should get wired up and then coated with epoxy so we can dunk it.

![image of pcb design](https://raw.githubusercontent.com/JeremyRuhland/turbidity_sensor/master/prototypes/rev1/optical_sensor_prototype.png)

Schematic is easily [viewable in pdf form](https://github.com/JeremyRuhland/turbidity_sensor/raw/master/prototypes/rev1/optical_sensor_prototype.pdf)

Calcuations
-----------

Infrared LED current limit:

    3.3V
     |
     R --- 1.69V drop & 70mA = 24.25Ohm @ 118mW
     |
    LED -- 70mA @ 1.6V & 112mW
     |
    FET -- 29mOhm * 70mA = 0.00203V & 142uW
     |
    GND

Photodiode transimpedance amplifier feedback:

Photodiode should have a reverse light current on the order of several microamps, a 10kOhm feedback resistor will amplify this into the range of tens of millivolts.
