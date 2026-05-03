# PHASE-RELEASE-LOGIC.md: Thermal/Hydration Trigger Data

This document outlines the specific environmental coefficients required to activate lipid release from the **KMLD** (Koji-Matrix Lipid Dispersion) lattice. It serves as a technical reference for engineers calibrating industrial equipment for "render-on-demand" performance.

---

## 1. Thermodynamic Release Profiles
The lipid payload remains sequestered within the vitrified starch wall until the system reaches the glass transition temperature ($T_g$).

### 1.1 Thermal Render Curves
Lipid release is a function of time and temperature. Below are the calibrated thresholds for standard **Yam-Starch** vitrification:

| Phase | Temperature Range | State Change | Lipid Flow Rate |
| :--- | :--- | :--- | :--- |
| **Dormant** | $< 55^\circ\text{C}$ | Vitrified / Glassy | $0\%$ (Total Sequestration) |
| **Activation** | $60^\circ\text{C} - 85^\circ\text{C}$ | Rubberization | Slow "Bleed" (Sweating) |
| **Peak Render** | $90^\circ\text{C} - 120^\circ\text{C}$ | Complete Dissolution | Full Release / High-Sizzle |

### 1.2 Elevated Smoke Point Stability
By sequestering the lipid within the chitin-rich koji matrix, the effective smoke point is elevated by approximately $15^\circ\text{C} - 20^\circ\text{C}$ compared to free-pour oils. The matrix acts as a thermal buffer, preventing rapid oxidation during high-heat applications.

---

## 2. Hydration Trigger Logic
Water acts as a plasticizer, instantly dropping the $T_g$ of the vitrified shield and allowing for room-temperature dispersion.

### 2.1 Moisture Sensitivity Thresholds
*   **Safe Storage Zone:** Water activity ($a_w$) must remain below $0.35$ to prevent premature lattice softening.
*   **Trigger Threshold:** Exposure to $a_w > 0.85$ (direct hydration) initiates barrier collapse within $3 - 5$ seconds.

### 2.2 Reconstitution Ratios
For instant sauce or roux applications, use the following weight-based hydration ratios:
*   **High-Viscosity Base:** $1:3$ (KMLD to Water).
*   **Low-Viscosity Emulsion:** $1:8$ (KMLD to Water).

---

## 3. Mechanical Shear Logic
In aerosol or high-speed extrusion environments, release is achieved through physical lattice fracture.

*   **Fracture Pressure:** The vitrified starch wall is engineered for brittle failure at pressures exceeding $15\text{ N/cm}^2$.
*   **Aerosol Applications:** Nozzle shear forces must be calibrated to break the outer starch shield without destroying the inner koji-mushroom scaffold, ensuring the flavor-burst effect occurs post-ejection.

---

## 4. Stability Validation
*   **Vitrification Integrity:** Sample must show zero lipid migration after 72 hours of exposure to $50^\circ\text{C}$ dry heat.
*   **Oxidative Audit:** Peroxide values must remain $\le 1.0\text{ meq/kg}$ after 12 months in nitrogen-flushed storage.
