# How to calibrate FT-5 with bltouch

1. Move nozzle to center, level platform using threaded rods. Ensure equal distance from the two railed T-slots to the platform below using a caliber.
2. [Manually level bed using the six thumb screws on the bottom of the platform. Move nozzle to each thumb screw position in a circular pattern at least twice.](https://youtu.be/0tt3ojJ9mMY)
   1. Validate tolerance of ~.1mm using auto grid level (G29)
3. [Find Z0 of nozzle to bed](https://youtu.be/y_1Kg45APko)
   1. Heat bed and nozzle
   2. Home Printer (G28)
   3. Move nozzle to bltouch XY position
   4. Move nozzle to Z0 position (G1 F60 Z0)
   5. Using a piece of paper on the bed, move the nozzle up/down until rubbing against the paper with some resistance.
   6. Calculate the ΔZ, minus the width of the paper and set new values. (M500, M501)

## Useful G Codes

| Code       | Description                      |
| :--------- | -------------------------------- |
| G28        | Home XYZ                         |
| G29        | Auto bed level (If you have one) |
| G1 F60 Z0  | Move Nozzle to datum             |
| M211 Z0    | Disable Z-min                    |
| M851 ZX.XX | Set New Z height                 |
| M211 S1    | Enable Z-min                     |
| M500       | Save Settings                    |
| M501       | Set Current Settings Active      |
| M503       | Get current Settings             |
| M114       | Vew Current position             |
