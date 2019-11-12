SMD 500+
Licensed under the TAPR Open Hardware License (www.tapr.org/OHL).
Copyright (c) Red Keg Technologies 2019.


Introduction
-------------------------------------------------------
The SMD 500+ project is a re-creation of the great Commodore Amiga 500/500+ using modern surface mounted components except for the CPU, custom chips, and CIAs.

The schematics are based on the schematics provided by Commodore in the Amiga 500+ user manual.
Each of the SMD components (except for the chip ram) was verified as available from Mouser in June 2019.  Anyone looking to construct the board would need a donor A500/A500+ or A2000 board in order to obtain the custom chips.


Features
-------------------------------------------------------
Certain experimental features have been added, most notably the ability to use either the 1 mb 8372 Agnus or the 2 mb 8375 Agnus, which are not pin-compatible with each other.  The board is set up to use the 8375 by default but can be changed simply by changing a couple of jumpers.

SVideo and Composite is supplied by an AD723 PAL encoder.  PAL only at this stage (sorry America).

The rechargeable battery has been substituted for a coin cell and diode (Aminet hack) and the RTC area has been slightly modified to allow for the RTC72421 IC to be used.

An option for a single HYB5118160BSJ 1Mx16 2 mb chip ram IC is available instead of using the eight 256kx4 TTH ICs.  The board is set up for the HYB5118160BSJ by default but can easily be changed with jumpers.  Note this modification is probably the most experimental of the lot and I am not 100% confident that there is not a mistake.

The power input socket is the same as Chucky Hertell's Re-Amiga 1200 board - i.e. you can use either the normal square DIN or a round DIN.

The EMF filters have been replaced with resistors and capacitors same as on the Amiga 1200.

Version 0.11 and 0.12 notes
-------------------------------------------------------
Minor revisions to fix a problem with the solder mask layer


Version 0.1 notes (also in the schematic)
-------------------------------------------------------

ADDED OPTION FOR ONE HYB5118160BSJ 1Mx16BIT CHIP RAM IC
REMOVED A501+ (PP12&13) FROM THESE SCHEMATICS 
(CONNECTOR P9 IS STILL THERE)

CHANGED BT9 TO COIN CELL AND DIODE
MINOR MODIFICATION TO ALLOW RTC72421

ADDED OPTION FOR AGNUS 8572.  CHANGE JP2 FOR 8572 
AND INSTALL FB101.1

ADD OPTION FOR ROUND DIN POWER INPUT

RESISTOR PACKS CHANGED FOR INDIVIDUAL RESISTORS

RTC REMOVED FROM A501 SCHEMATIC

REPLACED EMF FILTERS ON JOY1, JOY2, PARALLEL, SERIAL,
EXTERNAL FLOPPY, VIDEO OUT, CLOCKS, AUDIO, KB
WITH Rs, Cs, & FBs, A LA A1200

SVIDEO AND COLOUR COMPOSITE OUTPUT USING  AD723

U33.1 AND C33.1 REQUIRED IF USING AD723 OR 8372.

ONLY POPULATE EITHER U201 (2 MB SMD HYB5118160BSJ 1Mx16)
OR U16-23 (256Kx4 TTH FROM A500+).  

POPULATE C297-C299 FOR U201
POPULATE C16-C23 AND R209 FOR U16-U23

DO NOT INSTALL TRAP DOOR RAM WHEN U24 IS POPULATED

IF USING 1 MB AGNUS DO NOT INSTALL TRAP DOOR 
WHEN U20-23 ARE POPULATED

JUMPERS SET TO USE U201 AS DEFAULT
JP4 SET TO BYPASS U32 AS U201 HAS AN A9 LINE
JP98 CONNECTS THE TWO _RAS LINES

IF USING TTH 256Kx4 ICS (SAME AS ORIGINAL A500+ MACHINE)
POPULATE U32 AND BREAK JP4 AND JP98
JP3 SWAPS UPPER AND LOWER RAM BANKS FOR 256Kx4 CHIPS
