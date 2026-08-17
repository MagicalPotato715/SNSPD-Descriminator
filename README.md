IMPORTANT INFO:
-
- CTD is the Constant Threshold Discriminator, and contains two amplifiers and one comparator.
- Compute contains a Teensy 4.1 MCU (for counting and general control purposes) and DAC60501MDGSR DAC for CTD reference voltage.
- The single board with both CTD and compute, while possible to manufacture, is not recommended due to general price spiking over 10x10cm
- There may be slight physical mismatches between corresponding parts on CTD/compute and the single board.
- PCBA Essentials should be enough for ordering PCBA; the BOM sources from Mouser; however, most, if not all, components can be found on Digikey.
- When ordering PCBA for the compute board, make sure to separately order Teensy 4.1 boards with header pins already attached (or attach them yourself).
- 

Logistics:
- 
- ***Compute DAC may not Function Correctly***: In this case, J8 (bottom left corner) is hardware controlled through a voltage divider and the 200 ohm trim.
- ***Scalability***: Although the current compute board only features 6 JST conns, the Teensy 4.1 allows this to be expandable to ~30.
- ***CTD Hardware Troubleshooting***: The two LEDs should both light if both 3.3v and 5v respectively, are active. The test points can be used to troubleshoot signals.
- ***Ratbites on Single Board Not Snapping***: There is a chance for the ratbites to not work; the board still functions without the connection severed.
- ***Simulation***: The SPICE models in the single board folder should be enough to simulate; the models may be slightly outdated, look in "Misc files" if needed.
- ***Required Electronics***: The CTD requires a biased SNSPD pulse input via the correct coaxial cable; CTD and compute need to be connected by a 1x5 male-male JST wire with 2.5mm pitch; the compute board requires an external stable 5v source via coaxial cable; the CTD cannot function without 5v coaxial cable power.
