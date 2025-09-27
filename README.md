# Wireless Charging Receiver Dock

A DIY **wireless charging receiver dock**, designed to support the **QI protocol**, with **USB Type‑C male output**. When paired with a wireless charging transmitter, it enables most Type‑C devices to support wireless charging.

---

## 📐 Mechanical Specifications

* Diameter (with shell): **55.6 mm**
* Thickness: **6.1 mm**
* Weight: **16 g**
* Enclosure: 3D printed **PETG** shell

  * Print settings: **0.12 mm layer height**, random Z‑seam
  * Snap‑fit enclosure (tight, difficult to disassemble → assemble only after testing PCB)

---

## ⚡ Electrical Specifications

* Output: **5 V / 1 A**
* Tested stable power: **4.5 W continuous** (long‑term, no audible noise)
* Controller & resonant capacitors operate within datasheet thermal limits
* Receiver coil inductance: **12.6 µH** (common Qi receiver coil)

---

## 🔧 Design Notes

* **Thermal**: Large copper pours on the PCB improve heat dissipation.
* **Magnetic isolation**: Copper planes interfere with wireless charging recognition.

  * Solution: add **two ferrite sheets** → one between coil and copper pour, plus the coil’s own ferrite.
* **Capacitors**: Must use **X7R dielectric** (low temp‑drift) for resonant circuit.
* **Assembly**: No metallic screws in the enclosure (will disturb magnetic field). Shell is snap‑fit only.

---

## 📂 Repository Structure

```
Wireless-Charging-Receiver-Dock/
│
├── 3d shell/                # 3D printable PETG enclosure
├── Altium/                  # Altium source schematic & PCB files
├── BOM location/            # BOM with placement reference
├── Gerber_PCB1_2025-09-27/  # Gerber files for fabrication
├── result/                  # Rendered PCB and schematic images
│   ├── pcb (1).png
│   ├── pcb (2).png
│   └── ...
├── BOM_Board1_Schematic1_2025-09-27.csv  # BOM export (CSV)
├── BOM_charge_docker.xlsx                # BOM spreadsheet
├── SCH_Schematic1_2025-09-27.pdf         # PDF schematic
└── README.md
```

---

## 🖼️ Preview

### PCB Layout

![PCB Layout](result/pcb%20\(1\).png)

### Schematic Example

![Schematic](result/pcb%20\(2\).png)

---

## 🚀 Usage Instructions

1. Print the **PETG enclosure** using provided STL/3D files (0.12 mm layer height).
2. Assemble PCB, coil, and ferrite sheets into the enclosure.
3. Connect dock to a Qi transmitter pad.
4. Output available via **USB Type‑C male connector** at **5 V / 1 A**.

---

## ⚠️ Warnings

* Test bare PCB before inserting into snap‑fit shell.
* Always use **ferrite sheet isolation** between coil and copper pour.
* Do not use metal screws or metallic enclosure materials.

---

## 📑 License

Released under the **MIT License**.
You are free to fork, modify, and use in your own hardware builds.
