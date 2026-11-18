# mmWave Radar Station

**A camera-free experimental human-movement research platform based on 60 GHz millimetre-wave (mmWave) radar.**

> **Status (November 2026):** system architecture and hardware planning. Hardware integration and experimental results are pending. This project is **not** a validated fall-detection or emergency response device.

## Project scope

This repository documents the **standalone radar project** being developed for Hack Club Fabricate: an adjustable 60 GHz radar sensing station capable of collecting, visualising and analysing human-motion measurements in a controlled indoor environment.

The objective is to investigate whether radar point-cloud and tracked-object data can distinguish everyday movement from *fall-like events*, particularly near the floor and under different mounting conditions.

## Bill of materials (Fabricate)

**[Download the root-level BOM.csv](BOM.csv)** — itemised costs in USD, matching the latest radar-only Fabricate BOM shared for this project. Links point to the manufacturer or Australian retailers.

| Part | Qty | Unit cost (USD) | Line total (USD) | Funding | Supplier |
| --- | ---: | ---: | ---: | --- | --- |
| [TI IWR6843ISK-ODS radar](https://www.ti.com/tool/IWR6843ISK-ODS) | 1 | $235.55 | $235.55 | Grant | Texas Instruments |
| [Raspberry Pi 5 Model B 8GB](https://core-electronics.com.au/raspberry-pi-5-model-b-8gb.html) | 1 | $191.25 | $191.25 | Grant | Core Electronics |
| [Raspberry Pi 5 Active Cooler](https://core-electronics.com.au/raspberry-pi-5-active-cooler.html) | 1 | $6.00 | $6.00 | Grant | Core Electronics |
| [Official Raspberry Pi 5 27W USB-C power supply](https://core-electronics.com.au/raspberry-pi-5-power-supply-usb-c-pd-27w-white.html) | 1 | $14.20 | $14.20 | Grant | Core Electronics |
| Shipping, VAT, taxes and contingency | 1 | $36.80 | $36.80 | Grant | Provisional allowance |
| 3D-printed casings (self-supplied) | 1 | $0.00 | $0.00 | Already owned | Self-supplied |
| [Kingston Canvas Select Plus 64GB microSD card](https://www.umart.com.au/product/kingston-canvas-select-plus-64gb-100mb-s-microsd-card-with-adapter-sdcs3-64gb-89541) | 1 | $16.20 | $16.20 | Grant | Umart |
| **Total** | | | **$500.00** | | |

**Proposed grant-funded total: US$500.00.** The US$36.80 line is a provisional allowance for shipping, taxes and incidental order costs, **not an incurred expense**. Actual charges should be reconciled against receipts and the Fabricate BOM.

The 3D-printed mounting assembly and housings are original fabrication deliverables, made using existing resources. These are budgeted/proposed purchases, **not claims of completed fabrication or supplier stock availability**. Boot storage is included in the BOM through the Kingston 64GB microSD card. Check that necessary USB data cables are available or included with the ordered hardware.

## Engineering objectives

1. **Radar acquisition:** bring up the TI radar development board, inspect supported tracking demonstrations and capture timestamped point-cloud / track output.
2. **Mechanical design:** model and fabricate a secure radar housing and adjustable mounting bracket, with cable strain relief and unobstructed radar aperture.
3. **Mounting study:** compare overhead and high-wall arrangements, recording sensor height, tilt, tracked region and visibility near the floor.
4. **Activity experiments:** collect data for walking, sitting, bending, kneeling and lying down, as well as safely simulated fall-like transitions.
5. **Prototype classification:** explore interpretable radar-derived features and basic classification; distinguish fall-like events from confounding daily activities.
6. **Evaluation:** report event recall, false-alarm frequency, latency, tracking dropouts and sensitivity to furniture and placement changes.

Results will be reported only after experimental validation. Avoid leakage between overlapping windows from the same recording session when evaluating models.

## Proposed repository structure

```text
hardware/       CAD models, printed mounts, wiring and bill of materials
radar/          TI configurations, acquisition scripts and parsers
processing/     Radar-only activity features and prototype classifiers
experiments/    Test protocols, analyses and evaluation results
docs/           Setup instructions and engineering journal
```

Folders will be created as substantive files become available.

## Software and references

- [TI IWR6843ISK-ODS](https://www.ti.com/tool/IWR6843ISK-ODS)
- [TI Radar Toolbox](https://www.ti.com/tool/RADAR-TOOLBOX)
- [Raspberry Pi documentation](https://www.raspberrypi.com/documentation/)

## Safety and privacy

This is experimental human-activity research, **not** clinical fall detection. Do not rely on its output for emergency assistance. Obtain participant consent, use safe controlled test procedures and avoid publishing identifiable recordings or personal data.

## License

This repository includes an [MIT License](LICENSE). Review licensing separately for any future hardware design files and research datasets.
