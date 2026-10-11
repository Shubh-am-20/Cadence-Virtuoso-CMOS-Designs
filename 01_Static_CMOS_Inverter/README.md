# Static CMOS Inverter | 180 nm

Design, simulation, and physical verification of a **static CMOS inverter** using **Cadence Virtuoso** with the **GPDK 180 nm CMOS technology**. The experiment covers DC and transient analysis, propagation-delay measurement, layout verification, and pre-layout versus post-layout timing comparison.

## 1. Design Specifications

| Parameter | Value |
|:--|:--|
| Technology | GPDK 180 nm CMOS |
| EDA Tool | Cadence Virtuoso IC618 |
| Simulator | Cadence Spectre |
| Supply Voltage (VDD) | 1.8 V |
| Input Voltage Range | 0–1.8 V |
| NMOS (W/L) | 400 nm / 180 nm |
| PMOS (W/L) | 400 nm / 180 nm |

### Circuit Schematic

![CMOS Inverter Schematic](Schematics/CMOS_Inverter_Schematic.png)

## 2. Simulation Results

### DC Analysis

The voltage transfer characteristic (VTC) is obtained by sweeping the input voltage from **0 V to 1.8 V**.

![DC Transfer Characteristic](Simulation_Results/DC_Transfer_Characteristic.png)

### Transient Analysis

The input and output waveforms demonstrate the inverter's switching behaviour.

![Transient Response](Simulation_Results/Transient_Response.png)

### Propagation Delay

Propagation delays are measured at the **50% VDD crossing point (0.9 V)**.

**Average propagation delay:**

$$
t_p = \frac{t_{PHL} + t_{PLH}}{2}
$$

![Propagation Delay](Simulation_Results/Propagation_Delay.png)

## 3. Physical Layout and Verification

The inverter layout was implemented using the GPDK 180 nm technology design rules.

### Layout

![CMOS Inverter Layout](Layout/CMOS_Inverter_Layout.png)

### Verification Results

| Verification | Result |
|:--|:--|
| Design Rule Check (DRC) | ✅ Passed |
| Layout Versus Schematic (LVS) | ✅ Passed |
| Parasitic Extraction (PEX) | ✅ Completed |

## 4. Performance Comparison

| Parameter | Pre-Layout | Post-Layout |
|:--|--:|--:|
| tPHL (ps) | 21.9 | 15.0 |
| tPLH (ps) | 28.0 | 33.9 |
| Average Propagation Delay (ps) | 24.95 | 24.45 |
| Rise Time (ps) | 34.0 | 50.4 |
| Fall Time (ps) | 18.0 | 20.602 |

## 5. Key Observations

- **Propagation delay:** Post-layout tPHL decreased from **21.9 ps to 15.0 ps**, whereas tPLH increased from **28.0 ps to 33.9 ps**.
- **Average delay:** Average propagation delay remained nearly unchanged (**24.95 ps pre-layout** versus **24.45 ps post-layout**).
- **Rise/fall time:** Post-layout rise time increased by approximately **48.2%**, while fall time increased by approximately **14.5%**.
- **Physical verification:** The layout passed DRC and LVS, and parasitic extraction completed successfully.

> **Note:** The decrease in tPHL after extraction should be interpreted only after confirming that the pre-layout and post-layout testbenches use identical input slew, output load, supply voltage, and measurement criteria.

---

**Tools:** Cadence Virtuoso · Spectre · Assura · Quantus  
**Technology:** GPDK 180 nm CMOS
