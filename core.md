# Direct Fusion Propulsion (DFP) Core & Plasma Mixing Matrix

- **Reactor Topology:** Field-Reversed Configuration (FRC) open-ended magnetic mirror
- **Fuel Configuration:** Cryogenic Deuterium-Helium-3 ($^2\text{H} + ^3\text{He}$) injection loop
- **Magnetic Flux Density:** 4.5 to 7.0 Tesla via high-temperature REBCO HTS coils
- **Thrust Augmentation:** Multi-stage atmospheric mass entrainment channel

## 1. Confinement Mechanics & Controlled Leaking

The core confines a high-beta $^2\text{H} + ^3\text{He}$ plasma to execute an entirely aneutronic reaction cycle, yielding high-energy protons ($14.7\text{ MeV}$) and alpha particles ($3.6\text{ MeV}$). 

By dynamically adjusting the **Mirror Ratio ($R_m$)** at the aft throat nozzle, the flight system initiates an intentional plasma bleed to establish direct thrust:

$$R_m = \frac{B_{\text{max}}}{B_{\text{min}}}$$

The physical particle confinement duration ($\tau_c$) before escaping into the downstream expansion chamber is governed by the Gasdynamic Mirror law:

$$\tau_c = R_m \frac{L}{v_{\text{th}}} \ln\left(\frac{1}{\eta_{\text{anom}}}\right)$$

- $L$: Total length of the FRC magnetic containment container ($4.2\text{ m}$)
- $v_{\text{th}}$: Thermal velocity of escaping ions ($\sqrt{k_B T / m}$)
- $\eta_{\text{anom}}$: Anomalous cross-field transport diffusion coefficient

## 2. Atmospheric Mass Entrainment Matrix

At altitudes between 50,000 and 120,000 feet, the escaping core plasma ($v_p$) enters the mixing chamber, instantly ionizing incoming atmospheric air ($v_a$) via kinetic collision. The final exhaust velocity ($v_e$) utilizes mass entrainment to dramatically scale up total volumetric thrust ($T$):

$$v_e = \frac{\dot{m}_p v_p + \dot{m}_a v_a}{\dot{m}_p + \dot{m}_a}$$

$$T = (\dot{m}_p + \dot{m}_a) \cdot v_e$$

- $\dot{m}_p$: Mass flow rate of the cryogenic fusion core fuel injection
- $\dot{m}_a$: Mass flow rate of inhaled atmospheric air from the chined intake scoops

### 2.1 Low Altitude Operating Envelope (Dense Medium)
- The algorithm dampens $\dot{m}_a$ via variable magnetic choke geometry to prevent cooling (quenching) the core.
- Mirror Ratio $R_m$ is maximized to maintain tight internal confinement pressures.

### 2.2 High Altitude Operating Envelope (Thin Air / 50,000+ ft)
- Intake scoops open to maximum capture limits.
- $R_m$ drops to clear the magnetic throat, allowing the fusion plasma to expand violently through the Prandtl-Glauert nozzle for an effective cruise rating of **Mach 10–12**.

## 3. Traveling-Wave Direct Energy Feedback (TWDEC)

Energy to run the REBCO superconducting magnets is harvested electrostatically downstream in the nozzle shell, eliminating mechanical rotating assemblies:

$$P_{\text{ind}} = \frac{1}{2} \sigma B_{\text{nozzle}}^2 v_e^2 V_{\text{vol}} (1 - s)s$$

- $\sigma$: Electrical conductivity of the blended exhaust plasma
- $B_{\text{nozzle}}$: Magnetic flux density across the nozzle rings
- $V_{\text{vol}}$: Interaction cylinder volume
- $s$: Slip parameter optimized dynamically between $0.1$ and $0.3$

## 4. Hardware Safety & Containment Boundaries
- **Chamber Armor:** Single-piece monolithic Hafnium Carbide (HfC) matrix.
- **Thermal Shunt:** Liquid Deuterium pre-heaters snake through structural support struts, creating a regenerative cooling loop before fuel entering the core injection ports.
