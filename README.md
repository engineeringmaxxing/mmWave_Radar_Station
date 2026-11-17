# HearthSense

**Experimental privacy-preserving human activity sensing with 60 GHz mmWave radar and distributed Wi-Fi channel state information (CSI).**

> **Status (November 2026):** hardware planning and research setup. Detection performance is **not yet validated**. HearthSense is **not a medical device or emergency alert system**.

## Research question

Can combining radar tracking with distributed Wi-Fi CSI improve the robustness of detecting fall-like events compared with either sensing modality alone?

## Proposed hardware (V1)

| Hardware | Planned purpose |
| --- | --- |
| **TI IWR6843ISK-ODS** | 60 GHz radar point-cloud and movement tracking |
| **Raspberry Pi 5 (8 GB)** | Local data acquisition, logging, fusion and dashboard |
| **4 × ESP32-C5 boards** | Two transmitters and two receivers; up to four scheduled directed CSI links |
| **4 × Taoglas FXP830.07.0100C antennas** | Matched external Wi-Fi antennas |
| **3D-printed mounts and enclosures** | Repeatable placement and adjustable radar mounting |

**Important:** Confirm an external-antenna ESP32-C5 board such as **DFR1287 (ESP32-C5-U)** before buying; the similarly named **DFR1222** includes an onboard PCB antenna and does not directly accommodate the proposed U.FL antennas.

These are planned components, not a claim that the prototype is assembled or working.

## Research plan

1. **Radar baseline:** obtain TI point-cloud/tracking output; compare ceiling and wall mounting and furniture occlusion.
2. **CSI baseline:** establish one stable transmit–receive link, then expand to four nodes and validate packet scheduling.
3. **Multimodal acquisition:** ingest both sensor streams on the Raspberry Pi, monitor dropped samples, and establish time alignment.
4. **Controlled tests:** collect ordinary daily activities, rapid sitting, kneeling, lying down and safely simulated fall-like transitions.
5. **Evaluation:** compare radar-only, CSI-only and fusion models; report recall, false alarms per hour/day, detection latency and sensitivity to room changes.
6. **Hardware refinement:** develop mounting hardware and enclosures; consider custom PCBs only after acquisition is verified.

Use held-out sessions and, where feasible, participants and room configurations to limit dataset leakage.

## Planned repository structure

```text
hardware/       CAD, mounting designs, wiring, BOM
firmware/       ESP32 CSI capture and device configuration
radar/          TI configuration, parsers, radar experiments
wifi-csi/       CSI capture and signal processing
fusion/         Time alignment, classification and ablation studies
experiments/    Protocols, datasets metadata and metrics
docs/           Setup guides and research journal
```

These folders will be added as actual project files become available.

## References

- [TI IWR6843ISK-ODS](https://www.ti.com/tool/IWR6843ISK-ODS)
- [TI Radar Toolbox](https://www.ti.com/tool/RADAR-TOOLBOX)
- [Espressif ESP-CSI](https://github.com/espressif/esp-csi)
- [Raspberry Pi documentation](https://www.raspberrypi.com/documentation/)

## Safety, privacy and transparency

The system is an experimental platform for investigating **fall-like events** and must not be used as the sole basis for emergency response. Research participants should consent to data collection and to safe, controlled test procedures. Avoid publishing identifiable human data. A privacy-preserving end product is the design goal, not an already verified property.

## License

This repository currently includes an [MIT License](LICENSE) for software and associated documentation. Hardware design files and datasets may have separate licensing and privacy requirements.
