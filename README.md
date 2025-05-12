
# Optical Coherence Detector  
**An open-source tool for measuring phase-locked UV phenomena (e.g., auroras, ball lightning).**  

![Device Render](images/device_render.png) *[Show only housing exterior—no PCB close-ups]*  

## **Key Features**  
- **40Hz LCTF-modulated UV sensor** (Sony IMX487 + liquid crystal tunable filter)  
- **Helmholtz coil "environmental calibrator"** (0.1–10MHz)  
- **DSP validation** (Artix-7 FPGA confirms phase coherence)  
- **Open-hardware** (schematics, firmware, 3D models)  

---

## **Sanitized Block Diagram**  
```plaintext  
[UV Lens] → [300–450nm BPF] → [40Hz LCTF] → [IMX487]  
                                               ↓  
[Helmholtz Coils] → [DDS Driver] → [Artix-7 FPGA] → [SD Card]  
                                               ↑  
[3-Axis EMF] → [24-bit ADC]  
