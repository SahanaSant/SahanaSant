<p align="center">
  <img src="sources/giphy2welcome.GIF" width="380" />
</p>

<img src="sources/caterpillar.png" width="400" align="left" />

<br><br>

<div align="center">
  <p>
    <strong><em>whimsymaxxing at my desk .... ༻*ੈ✩‧₊˚</em></strong>
    <img src="sources/giphy.gif" width="400" />
    <br><br>
    ELECTRICAL ENGINEERING @ UCALGARY
    <br>
    embedded systems • control systems • low-level IC.
    <br>
    ૮₍ ´ ꒳ `₎ა
  </p>
</div>

<br><br>
<br clear="left" />

## 🧵 things i've built

<p align="center"><sub><em>(the short, honest version — click a title for the actual code)</em></sub></p>

### [Schulich on Chip — RISC-V SoC Verification](https://github.com/Schulich-on-a-Chip/core-v-mcu)
![SystemVerilog](https://img.shields.io/badge/SystemVerilog-8B5CF6?style=flat-square) ![cocotb](https://img.shields.io/badge/cocotb-2E8B57?style=flat-square) ![LibreLane](https://img.shields.io/badge/LibreLane-RTL--to--GDS-2563EB?style=flat-square)

- hardened peripheral RTL (UART, I²C, I²S, uDMA) on an open-source CORE-V-MCU SoC
- verified it with cocotb testbenches, then pushed modules through the LibreLane RTL-to-GDS flow
- currently running a variety of tests on the numerous protocols of the RTL on the beloved basys3! 

### [muzic-player — Embedded Audio Player & Visualizer](https://github.com/SahanaSant/muzic-player)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square) ![ESP32--S3](https://img.shields.io/badge/ESP32--S3-E7352C?style=flat-square) ![FreeRTOS](https://img.shields.io/badge/FreeRTOS-4B8BBE?style=flat-square)

<p align="center">
  <img src="sources/muzic-player-ui.png" width="320" />
</p>

- touchscreen WAV player with a radix-2 Cooley–Tukey FFT I wrote from scratch, driving a live 13-band spectrum visualizer
- windowing + DC removal clean up 1024-sample snapshots of the raw PCM stream before each transform
- FFT bins grouped into log-spaced bands (20 Hz–16 kHz), peak power per band → bar height
- runs on its own low-priority FreeRTOS task so it never once stutters the audio it's dancing to

### [Nrf52840-Midi-Visualizer](https://github.com/SahanaSant/Nrf52840-Midi-Visualizer)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square) ![Zephyr_RTOS](https://img.shields.io/badge/Zephyr_RTOS-744DA9?style=flat-square) ![LVGL](https://img.shields.io/badge/LVGL-FF6B00?style=flat-square)

<p align="center">
  <img src="sources/midi-visualizer-bars.png" width="260" />
  &nbsp;&nbsp;
  <img src="sources/midi-visualizer-modes.png" width="420" />
</p>

- MIDI file parser I wrote byte-by-byte, no external library — raw header/track chunks, variable-length delta-times, running status, tempo and note events
- feeds a 12-band EQ and piano-mode visualizer on an nRF52840
- notes sorted bass-to-treble with a velocity-weighted histogram, not a flat 12-way split

**how piano mode maps notes → keys:**
- each frame scans the 12 EQ bars for the 3 strongest
- 2 loudest → white keys (bar index 0–11 maps proportionally across the 14 white keys, bass left, treble right)
- 3rd bar, if close in volume to the 2nd, lights a black key the same way
- glow brightness scales with that bar's amplitude and fades over time — a note struck and let go, not a flat blink

<br>

## ⚙️ tech stack

<h3 align="center">Languages & Technical Computing</h3>

<p align="center">
  <img src="https://skillicons.dev/icons?i=c&theme=dark" width="72" height="72" alt="C" title="C" />
  &nbsp;&nbsp;
  <img src="https://skillicons.dev/icons?i=py&theme=dark" width="72" height="72" alt="Python" title="Python" />
  &nbsp;&nbsp;
  <img src="https://skillicons.dev/icons?i=java&theme=dark" width="72" height="72" alt="Java" title="Java" />
  &nbsp;&nbsp;
  <img src="https://skillicons.dev/icons?i=matlab&theme=dark" width="72" height="72" alt="MATLAB" title="MATLAB" />
  &nbsp;&nbsp;
  <img
  src="https://api.iconify.design/file-icons/systemverilog.svg?color=%238B5CF6"
  width="72"
  height="72"
  alt="SystemVerilog"
  title="SystemVerilog"
  />
</p>

<h3 align="center">Digital Hardware & Chip Design</h3>

<p align="center">
  <a href="https://www.amd.com/en/products/software/adaptive-socs-and-fpgas/vivado.html">
    <img src="https://github.com/Xilinx.png" width="72" height="72" alt="AMD Vivado" title="AMD Vivado" />
  </a>
  &nbsp;&nbsp;
  <a href="https://www.kicad.org/">
    <img src="https://github.com/KiCad.png" width="72" height="72" alt="KiCad" title="KiCad" />
  </a>
  &nbsp;&nbsp;
  <a href="https://github.com/librelane/librelane">
    <img src="https://github.com/librelane.png" width="72" height="72" alt="LibreLane" title="LibreLane" />
  </a>
</p>

<p align="center">
  <sub><b>AMD Vivado &nbsp;&nbsp;•&nbsp;&nbsp; KiCad &nbsp;&nbsp;•&nbsp;&nbsp; LibreLane</b></sub>
</p>

<h3 align="center">Industrial Engineering</h3>

<p align="center">
  <img src="https://skillicons.dev/icons?i=autocad&theme=dark" width="72" height="72" alt="AutoCAD" title="AutoCAD" />
  &nbsp;&nbsp;
  <a href="https://www.bentley.com/software/">
    <img src="https://github.com/BentleySystems.png" width="72" height="72" alt="MicroStation and ProjectWise" title="MicroStation and ProjectWise" />
  </a>
  &nbsp;&nbsp;
  <a href="https://www.cognite.com/en/product/cognite-data-fusion/kognitwin">
    <img src="https://github.com/cognitedata.png" width="72" height="72" alt="Kognitwin" title="Kognitwin" />
  </a>
</p>

<p align="center">
  <sub><b>AutoCAD &nbsp;&nbsp;•&nbsp;&nbsp; MicroStation &nbsp;&nbsp;•&nbsp;&nbsp; ProjectWise &nbsp;&nbsp;•&nbsp;&nbsp; Kognitwin</b></sub>
</p>

<h3 align="center">Development Tools</h3>

<p align="center">
  <img src="https://skillicons.dev/icons?i=git&theme=dark" width="72" height="72" alt="Git" title="Git" />
  &nbsp;&nbsp;
  <img src="https://skillicons.dev/icons?i=github&theme=dark" width="72" height="72" alt="GitHub" title="GitHub" />
  &nbsp;&nbsp;
  <img src="https://skillicons.dev/icons?i=vscode&theme=dark" width="72" height="72" alt="VS Code" title="VS Code" />
</p>

### 🎧 currently

currently in school, perchance building something (☞ ͡° ͜ʖ ͡°)☞
