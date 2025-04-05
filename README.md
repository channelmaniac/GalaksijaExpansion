# Galaksija Expansion
Expansion edge connector for the Galaksija computer
--------------------

The Galaksija is a Z80-based computer from the former country of Yugoslavia, circa 1983. 

It's an easy to build replica, but does have some quirks to get running and has an odd edge connector profile
that doesn't match any known connector that I've ever seen. Turns out, back in the 80s a magazine article 
contained a layout for an adapter that would convert the pin connections to a bog standard 44-pin card-edge.

You can find that article on the Internet Archive here: 
https://archive.org/details/Racunari_Magazine_1984_01/page/n55/mode/2up

I've taken that PCB photo-etch layout from the magazine and put it into gerbers using KiCAD. Somehow, laying
it out by eye, I nailed it the first time - time to go buy a lottery ticket! Use your favorite PCB fab to 
have these made. The vias are not covered by silkscreen so you can solder the necessary wires to them to 
connect this to the PCB. Use a small fiber or plastic washer to offset it from the main PCB and bolt it to
the PCB using the larger two holes then solder wires to connect each hole to the main PCB. You could use
individual 2.54mm pins if you wish.

Feel free to make/sell/whatever you want, but please give me credit for the work. Many thanks to Con Skordis
for the VIP COSMAC edge connector object in KiCAD which was modified to use here. All signals are clearly
labeled on the edge connector. The big segment with all the grounds is on the top side.

Now for the quirks... In building the computer, the clock divider circuit did not work properly, giving me
24KHz for horizontal sync and 75Hz for vertical. The Fairchild 74LS93 chip was the culprit. Tried swapping
it out with another one but had the smae results. I put a TI branded SN74LS93 in and the timing circuit 
behaved as it should and I had proper video sync. Next was that graphics were corrupt. The 5n bodge cap on
the CPU didn't work for me. I tried several progressively smaller caps and found the 470pf worked perfect
and cleaned up the graphics on the screen.

Enjoy your build and I hope this project makes it easier to connect memory and other expansions to it.
