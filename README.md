# version1

version1 is a TKL(TenKeyLess) Mechanical Keyboard with Kalih Hotswappable sockets and Cherry MX Black switches.
This keyboard was designed as a deep dive into electronics as a beginner and to learn more about CAD.
The keyboard features a fully custom made PCB with 87 standard TKL keys and 4 macrokeys. The keyboard is wired, using a USB-C port.
version1 uses the STM32F072CBT6 at its core.

The PCB was designed in KiCad and the case was designed in Autodesk Fusion. Fusion was also used to render images of the design.
The footprints for the switches have been taken from the marbastlib library - https://github.com/ebastler/marbastlib

Note: This is still a WIP. Please copy anything at your own risk or do not copy at all.

## Repository Guide
```
version1/
|── PCB/
|   |── version1.kicad_pro
|   |── version1.kicad_pcb
|   |── version1.kicad_sch
|   └── version1_matrix.kicad_sch
|
|── CAD/
|   |── version1.f3d
|   |── version1-assembly.step
|   |── version1.fbx
|   |
|   |──── version1-base/
|   |     |── version1-base-left.step
|   |     |── version1-base-middle.step
|   |     └── version1-base-right.step
|   |
|   └──── version1-plate/
|         |── version1-plate-left.step
|         └── version1-plate-right.step
| 
|── Production/   
|    |── gerbers.zip/
|    |
|    |── STL Files/
|    |   |─── version1-base/
|    |   |    |── version1-base-left.stl
|    |   |    |── version1-base-middle.stl
|    |   |    └── version1-base-right.stl
|    |   |
|    |   └─── version1-plate/
|    |        |── version1-plate-left.stl
|    |        └── version1-plate-right.stl
|    |
|    └── STEP Files/
|           |─── version1-base/
|           |      |── version1-base-left.step
|           |      |── version1-base-middle.step
|           |      └── version1-base-right.step
|           |
|           └──── version1-plate/
|                   |── version1-plate-left.step
|                   └── version1-plate-right.step
|
|── Assets/
|    |── Keycaps/
|    |── MX Switch/
|    |── Rotary Encoder/
|    |── Type-C/
|    └── version1.fbx
|
|── qmk_firmware/
|    |── version1/
|       |── keymaps/
|       |   |── keymaps/
|       |       └── default/
|       |           └── keymap.c
|       |── config.h
|       |── keyboard.json
|       └── readme.md
|
|── BOM.csv
|── Zine.pdf
└── README.md
```

## Schematic
##### Overall Schematic
<img width="1174" height="810" alt="image" src="https://github.com/user-attachments/assets/b66b5bd6-ac15-4012-9690-213726f1612f" />

##### Key matrix
<img width="1125" height="765" alt="image" src="https://github.com/user-attachments/assets/8db83b8f-6b9c-4ddd-8eda-fd39123e0d0b" />

## PCB
##### PCB Front without GND Plane
<img width="1563" height="540" alt="image" src="https://github.com/user-attachments/assets/6807294e-639c-4b0d-8790-0f17afbe6356" />

##### PCB Front with GND Plane
<img width="1579" height="554" alt="image" src="https://github.com/user-attachments/assets/8efa5896-a019-4117-9711-0cc2a10932f5" />

##### PCB Back without GND Plane
<img width="1561" height="547" alt="image" src="https://github.com/user-attachments/assets/2e04a868-2f80-4ca1-917e-a8f28207c9be" />

##### PCB Back with GND Plane
<img width="1579" height="557" alt="image" src="https://github.com/user-attachments/assets/783df441-0199-496c-92f0-c4b2f12ca915" />

## CAD
The case has been split into two parts on the plate and 3 parts on the base to accomodate 3D printed parts. The plates and base have small pegs and holes for assembly.

#### Full Assembly
##### Top View
<img width="1193" height="477" alt="image" src="https://github.com/user-attachments/assets/92e03811-2af7-43de-a6d6-1e1489296483" />

#####  Side View
<img width="972" height="529" alt="image" src="https://github.com/user-attachments/assets/5498981b-a3c0-47a0-b9e8-e2cc2284cbea" />

#### Top Plate
##### Top View
<img width="1270" height="508" alt="image" src="https://github.com/user-attachments/assets/4043ad0f-5233-4d82-976a-fa9fa0e7830c" />

#####  Side View
<img width="1430" height="548" alt="image" src="https://github.com/user-attachments/assets/297aeba1-6ec4-47cc-9f11-5a037c634ba1" />

#### Base
##### Top View
<img width="1220" height="478" alt="image" src="https://github.com/user-attachments/assets/b6198f00-43ee-4a7c-8859-f6568127d678" />

#####  Side View
<img width="1222" height="689" alt="image" src="https://github.com/user-attachments/assets/aad6137b-1a00-47fa-80c9-22d5fecffeab" />

## Renders [to add]
##### Top view

##### Side view

## Build Guide
To be updated after IRL build.

## Bill of Materials
# Bill of Materials

| MPN | Designator | Quantity | Unit Price (USD) | Price (Ext.) | Package | LCSC Part Number | Link |
|-----|------------|----------|-----------------|--------------|---------|-----------------|------|
| CPG151101S11-2 | MX1-M91 | 100 | 0.0344 | 3.44 | - | C49352235 | https://www.lcsc.com/product-detail/C49352235.html |
| STM32F072CBT6 | U1 | 1 | 2.212 | 2.21 | LQFP-48(7x7) | C81720 | https://www.lcsc.com/product-detail/C81720.html |
| XC6206P332MR-G | U2 | 5 | 0.1119 | 0.56 | SOT-23-3L | C5446 | https://www.lcsc.com/product-detail/C5446.html |
| PRTR5V0U2X-ES | D1 | 5 | 0.0404 | 0.2 | SOT-143 | C5180302 | https://www.lcsc.com/product-detail/C5180302.html |
| 1N4148W | D2-D93 | 100 | 0.0058 | 0.58 | SOD-123 | C917030 | https://www.lcsc.com/product-detail/C917030.html |
| TYPE-C 16PIN 2MD(073) | J1 | 20 | 0.0747 | 1.49 | SMD | C2765186 | https://www.lcsc.com/product-detail/C2765186.html |
| TS-1088-AR02016 | SW1, SW2 | 10 | 0.0538 | 0.54 | SMD, 4x3mm | C720477 | https://www.lcsc.com/product-detail/C720477.html |
| EC11E15244B2 | SW3 | 1 | 2 | 2 | Through Hole | C470754 | https://www.lcsc.com/product-detail/C470754.html |
| 1206L050YR | F1 | 10 | 0.0622 | 0.62 | 1206 | C163512 | https://www.lcsc.com/product-detail/C163512.html |
| RC0402FR-075K1L | R1, R2 | 100 | 0.0009 | 0.09 | 0402 | C105872 | https://www.lcsc.com/product-detail/C105872.html |
| RC0402FR-0710KL | R3 | 100 | 0.0008 | 0.08 | 0603 | C60490 | https://www.lcsc.com/product-detail/C60490.html |
| CC0402KRX7R7BB104 | C1, C4, C5, C6, C7, C8, C10 | 100 | 0.0011 | 0.11 | 0402 | C60474 | https://www.lcsc.com/product-detail/C60474.html |
| CL10B105KA8NNNC | C2, C3 | 50 | 0.0069 | 0.35 | 0603 | C29936 | https://www.lcsc.com/product-detail/C29936.html |
| CL10A106KP8NNNC | C9 | 50 | 0.0103 | 0.52 | 0603 | C19702 | https://www.lcsc.com/product-detail/C19702.html |
| Cherry MX Black Switches [Pack of 10] | - | 10 | 3.48 | 34.8 | - | - | https://neomacro.in/products/cherry-mx-switches?_pos=2&_sid=a9445e82d&_ss=r&variant=47150319108374 |
| Keycaps | - | 1 | 13.5 | 13.5 | - | - | https://stackskb.com/store/veekos-gradient-keycaps-cherry-profile-135-keys/ |
| Stabilizers (clip in) | - | 10 | 0.33 | 3.32 | - | - | https://neomacro.in/products/cherry-pcb-mount-stabilizers-clip-in?_pos=1&_sid=0547a7463&_ss=r |
| Wires for stabilizers | - | 1 | 4.16 | 4.16 | - | - | https://neomacro.in/products/equalz-c3-stabilizer-wire-set |
| M3x20mm Screws | - | 15 | 0.017 | 0.26 | - | - | https://omrook.com/ss-allen-csk-m3-x-20mm-dia-3mm-length-20mm-stainless-steel-ss202-allen-socket-countersunk-screws/ |
| M3x4 Brass Inserts | - | 50 | 0.023 | 1.15 | - | - | https://omrook.com/m3-x-4-brass-threaded-inserts-nut-50pc/ |
| Rotary Encoder Knob [Pack of 5] | - | 1 | 0.033 | 0.17 | - | - | https://makerbazar.in/products/black-rotary-encoder-knob-111-no |
| PCB - JLCPCB (with shipping) | - | 5 | 9.552 | 47.76 | - | - | https://jlcpcb.com/ |
| Total |  |  |  | 117.91 |  |  |  |