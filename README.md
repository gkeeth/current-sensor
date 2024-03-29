# current-sensor
Hall effect current sensor board. Invasive (connected in series with DUT), with BNC output to oscilloscope.

Designed to fit in Hammond 1593W enclosure. Powered by 9V battery. Includes PCBs for front and back panels (20A and 36A options for front panel).

## Specifications:
- Output: 0-5V, DC-coupled
- Maximum input current: +/-20A. Different current limits are possible by
selecting a different version of the ACS730 Hall effect IC (also changes sensitivity)
  - ACS730xxxxx-20AB: +/- 20A
  - ACS730xxxxx-40AB: +/- 40A [limited to 36A by binding posts]
- Gain: selectable between x1, x10, and x100
  - -20AB: x1 (100mV/A), x10 (1V/A), and x100 (10V/A)
  - -40AB: x1 (50mV/A), x10 (500mV/A), and x100 (5V/A)
- Bandwidth: selectable between 1kHz, 10kHz, and 100kHz
- Power supply: 9V battery

## Adjustment Procedure:
The only adjustment needed is to adjust the zero-current offset voltage so that
the output reads zero when zero current is applied to the input.

1. Disconnect wires from input jacks so that input current is zero.
2. Set Gain to 1x and Bandwidth to 1kHz.
3. Adjust trimmer RV1 until the voltage at the output (between BNC center pin
and shell) is as close to 0V as possible.
4. Increase gain to 10x/100x and fine-tune adjustment.

## Possible Future Improvements:
- use a multi-turn trimpot for zero-current offset adjustment
- make adjustment trimpot available at rear panel for trim without removing case

## Schematic:
[PDF of schematic](pdf/current-sensor.pdf)
![schematic](img/current-sensor.svg)

## Layout:
![layout](img/layout.png)

## BOM:
[BOM for main board](bom/current-sensor.csv)

### Additional components:
Note that the board was designed with Molex SL crimp terminals for the LED and 9V battery,
but those connections could be done with another crimp family or even soldered. Substitute
connectors as appropriate.

| Quantity | Manufacturer | Manufacturer PN  | Distributor | Distributor PN | Notes                |
| -------- | ------------ | ---------------- | ----------- | -------------- | -------------------- |
| 1        | Hammond      | 1593WBK          | Digikey     | 164-1593WBK-ND | case                 |
| 1        | Hammond      | 1593ATS50        | Digikey     | HM1442-ND      | PCB mounting screws  |
| 1        | MPD          | BH9VW            | Digikey     | BH9VW-ND       | battery holder       |
| 2        | Cal Test     | CT2232-4         | Digikey     | BKCT2232-4-ND  | binding posts        |
| 1        | C&K          | G003G            | Digikey     | 401-1205-ND    | power button cap     |
| 1        | Lumex        | SSI-LXH312ID-150 | Digikey     | 67-1190-ND     | power LED            |
| 2        | Molex        | 0190050010       | Digikey     | WM18241-ND     | QC connectors        |
| 4        | Molex        | 0016020097       | Digikey     | WM2513-ND      | SL crimp terminals for LED and battery |
| 2        | Molex        | 0050579402       | Digikey     | WM2900-ND      | SL crimp housings for LED and battery  |


## Front/Rear Panel and Assembly:
![front panel](img/render_frontpanel.png)
![back panel](img/render_backpanel.png)
![front render](img/render_overview.png)

## License:
Licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
