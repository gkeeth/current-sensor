# current-sensor
Hall effect current sensor board. Invasive (connected in series with DUT), with BNC output to oscilloscope.

WORK IN PROGRESS

Specifications:
- Output: 0-5V, DC-coupled
- Maximum input current: +/-40A. Different current limits are possible by
selecting a different version of the ACS730 Hall effect IC (also changes sensitivity)
- Gain: selectable between x1 (50mV/A), x10 (500mV/A), and x100 (5V/A)
- Bandwidth: selectable between 100kHz, 10kHz, and 1kHz

Designed to fit in Hammond 1593W enclosure. Includes PCBs for front and back panels.


![schematic](img/current-sensor.svg)
![layout](img/layout.png)
![front render](img/render_front.png)
![back render](img/render_back.png)

Licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
