## Static CMOS Inverter | 180 nm

Design, simulation, and physical verification of a Static CMOS Inverter using Cadence Virtuoso with GPDK 180 nm CMOS technology. The experiment focuses on DC characteristics, propagation delay, physical layout, and pre-layout versus post-layout performance.

## 1. Design Specifications

| Parameter Value |
| --- |
| Technology GPDK 180 nm CMOS EDA Tool Cadence Virtuoso IC618 Simulator Cadence Spectre Supply Voltage (VDD) 1.8 V Input Voltage Range 0–1.8 V NMOS (W/L) 400 nm / 180 nm PMOS (W/L) 400 nm / 180 nm |

## 2. Simulation Results

## DC Analysis

Voltage Transfer Characteristic (VTC) obtained by sweeping the input voltage from 0 V to 1.8 V.

## Transient Analysis

Input and output waveforms demonstrating the switching behaviour of the inverter.

## Propagation Delay

Propagation delays are measured at the 50% VDD crossing points (0.9 V). Average delay: tp = (tPHL + tPLH) / 2.

## 3. Physical Layout & Verification

The inverter layout was implemented using the GPDK 180 nm technology design rules.

## Verification Results

| Verification Result |
| --- |
| Design Rule Check (DRC) Passed Layout Versus Schematic (LVS) Passed Parasitic Extraction (PEX) Completed |

## 4. Performance Comparison

| Parameter Pre-Layout Post-Layout |
| --- |
| tPHL (ps) 21.9 15.0 tPLH (ps) 28.0 33.9 Average Propagation Delay (ps) 24.95 24.45 Rise Time (ps) 34.0 50.4 Fall Time (ps) 18.0 20.602 |


## 5. Key Observations

- Propagation delay: Post-layout tPHL decreased from 21.9 ps to 15.0 ps, while tPLH increased from 28.0 ps to 33.9 ps.

- Average delay: Mean propagation delay remained nearly unchanged at approximately 24.5 ps.

- Rise/fall times: Post-layout rise time increased by approximately 48.2%, while fall time increased by approximately 14.5%.

- Physical verification: The layout passed DRC and LVS, and parasitic extraction was completed.

- Technology: GPDK 180 nm CMOS

Tools: Cadence Virtuoso | Spectre | Assura | Quantus
