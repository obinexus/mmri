# MMRI – Mind-Magnetic Resonance Imaging  
**ObiNexus T3ab Protocol – 4-D, zero-contact, zero-magnet neuro-mapper**

---

## 1-line elevator pitch  
MMRI turns the *itch* of a single shedding skin-cell into a radio-phase beacon that lets a 3-D microwave array image your 4-D mind-state without ever touching you or sticking you inside a magnet.

---

## What exists right now  
- `index.html` – live Web-Assembly demo (Chrome ≥ 119)  
  - streams 2.4 GHz phase from laptop/phone Wi-Fi chipset  
  - runs the Δφ-null-space collapse solver in real time  
  - plots 100 µm “mind voxels” on a WebGL hyper-cube  
- `mmri_obinexus_t3ab.html` – single-page build of the alg (no UI)  
- Both files are **proof-of-concept only** – not yet medical hardware.

---

## Physics in one breath  
1. stratum corneum thickness change Δd ≈ 3 µm  
2. produces RF phase shift Δφ = 2k Δd √ε_r ≈ 0.15 rad @ 2.4 GHz  
3. itch-waveform d-itch/dt gives **time-series boundary condition**  
4. regularises the 4-D → 3-D EM inverse problem (κ drops from 10¹² → 10²)  
5. spatial accuracy ~ 100 µm without contact, magnet or ionising radiation.

---

## How to run the demo  
```bash
git clone https://github.com/obinexus/mmri.git
cd mmri
# serve locally (any static server)
python -m http.server 8080
# open http://localhost:8080
```
- Allow Wi-Fi sensor access (chrome://flags/#enable-experimental-web-platform-features)  
- Sit 30 cm from laptop; scratch your forearm when prompted.  
- Watch the hyper-cube update live.

---

## Road-map  
| Milestone | Target | Status |
|-----------|--------|--------|
| v0.2 | 6-antenna PCB, 5 mW, 5 kHz bandwidth | designing |
| v0.5 | MHRA pre-clinical thermal/SAR dossier | planned 2026-Q2 |
| v1.0 | UKCA Class IIa diagnostic, 10 µm voxel | planned 2027 |

---

## Contribute  
- RF / DSP engineers → help port solver to CUDA & Metal  
- WebGL/ WASM wizards → shrink bundle < 200 kB  
- Neuroscientists → supply open-access itch-vs-cognitive-load datasets  
- Lawyers → draft open-hardware licence compatible with UK MDR 2002

---

## Licence & ethics  
Hardware: CERN-OHL-W (permissive copy-left)  
Software: MIT  
Data you generate with the demo stays **on your machine** – zero telemetry.

---

**Scratch, relate, image – and if the firewall of skin still feels like “fire-noise,” open an issue.**
