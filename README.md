# AY-3-8910 adapter for the Amstrad CPC

The sound chip AY-3-8912 as used in the Amstrad CPC is hard to find and often quite expensive. With this adapter it is possible to use the MUCH cheaper and easily available AY-3-8210A sound chip in the Amstrad CPC.

<img src="/pictures/PCB.jpg" width="500"/>

The adapter works in all 3 CPC models (464,664 and 6128). The PCB layout was defined by the limiting space in the CPC 6128 but it will of course perfectly fit into the 464 and 664 too.

> [!IMPORTANT]
> This adapter is ONLY for Amstrad CPC as it is using a slightly different footprint for the sound chip than other computers. It will also not fit into the Amstrad Plus and GX4000 models. 

## AY-3-8910 vs AY-3-8910A

The AY soundchips with the suffix A in their model number slightly differ from their counterparts without the A suffix: The AY-3-8912 as used in the CPC does have internal pull-up resistors on its datalines, 
the counterparts with the A suffix are lacking this internal pull-up. To use the -A variants in the CPC it's required to add pull-up resistors to the data lines. 

## License

The project is released under the CC BY-NC-ND 4.0 license with the following enhancements: The expansion and all resources are free to use for personal use. Selling this PCB in any form (alone, as a DIY bundle or fully built) for a profit is strongly forbidden, however it may be used in commercial repairs as long as the PCB itself won't be charged for (you may charge for the repair and the other materials of course). For an exception please contact me.

## Building a AY-3-8912 replacement

For a full assembly you need 
- basic soldering skills - as long as you can solder normal through hole components reliably, you will be fine.

### Disclaimer

> [!CAUTION]
>**USE AT YOUR OWN RISK.**
>
>This is a hobby project, I am a hobbyist and no engineer. There is always the risk that the use of this adapter, the different components used or the repair itself can cause harm to your CPC. 
>Although I have tested this adapter on several CPCs for many hours with many other expansions and lots of software, there is no guarantee that it will properly work under all circumstances in your CPC.
>
>Especially if you are building this for others (commercially or not) make sure to make your own intense tests to guarantee this adapter works as expected before handing over to the recipients.  
>
>**USE AT YOUR OWN RISK.** 

### Bill of Materials

| Part | Quantity |
| --- | --- |
| PCB | 1 |
| AY-3-8910(A)<br><sup>or compatible</sup>| 1 |
| IC socket 28pin<br><sup>(not on 6128!)</sup> | 1 |
| Resistor Array 10k - 9 pins<br><sup>only needed for AY-3-8910A</sup> | 1 |
| Pin Header 1x14 | 2 | 

### PCB

You can order PCBs easily here: [https://www.pcbway.com/project/shareproject/...](https://www.pcbway.com/project/shareproject/Amstrad_CPC_AY_3_8910_adapter_2887f427.html)

### Build

1) start with the pin headers on bottom of the PCB. Some pin headers need to be adjusted slightly as usually one side of the pin headers is too short and the other too long. You can move the plastic bar with e.g. pliers easily. Move them until the plastic bar almost reaches the mid of the pin header. One side should be slightly shorter than the other side. The short side will be the one that is later plugged into the CPU socket on the motherboard.
2) only if required: add the resistor array on bottom of the PCB. Pay close attention to the orientation of the resistor array. The little dot on the resistor array must be aligned with the rectangular soldering point on the PCB. 
3) 464/664: from top, add the socket. Put the AY-3-8910 into the socket<br>6128: solder the AY-3-8910 directly to the PCB (space constraints in the 6128 don't allow to add a socket)
4) Follow this guide on the CPC Wiki on how to replace ICs on the CPC mainboard: https://www.cpcwiki.eu/index.php/IC_Repair

## A second I/O port

The AY-3-8910 offers two I/O ports instead of the one on the AY-3-8912. The additional data pins for the second I/O port can be accessed on the PCB. For accessing the I/O port refer to the AY-3-8910 data sheet.

