# matrix_logic.md: Technical Guide for Variable Lipid Loading

This document defines the mathematical constraints for maintaining structural integrity within the **FAT-OS** architecture. Adherence to these ratios ensures that the "Physical Walls" do not collapse during the vitrification process or undergo premature lipid leakage.

---

### 1. Lipid Loading Factor ($L_f$)
To maintain lattice integrity and prevent sequestration failure, the lipid payload is governed by the following maximum coefficient:
*   **Formula:** $L_f \le 2.5 \times (W_s + W_b)$.
*   **Definition:** The total lipid payload must not exceed 2.5 times the combined dry weight of the **Scaffold** ($W_s$) and the **Barrier** ($W_b$).
*   **Constraint:** Exceeding this factor results in "weeping" where the internal pressure of the lipid droplets overcomes the structural strength of the vitrified wall.

---

### 2. Vitrification Calculation (Surface Area Mapping)
The application of the secondary barrier is not a weight-fixed variable but a surface-area-dependent calculation.
*   **Protocol:** The starch barrier weight is calculated based on the total surface area of the dehydrated koji-scaffold.
*   **Objective:** To ensure a total oxidative seal that is consistent across different particle sizes and scaffold geometries.
*   **Metric:** A continuous glassy film of $\ge 5$ microns is required to achieve the mandated **Vitrification Grade** status.

---

### 3. Cation Balancing for Emulsion Stability
For high-umami profiles, the interaction between the koji-matrix and the lipid must be stabilized via mineral titration.
*   **Divalent Cations:** Calcium ($Ca^{2+}$) or Magnesium ($Mg^{2+}$) must be utilized to bridge the biological scaffold and the lipid interface.
*   **Standard Ratio:** Titrate at a ratio of $0.05:1$ against the total lipid mass.
*   **Function:** This ensures proper emulsion stability prior to dehydration, preventing lipid coalescence during the transition to the glassy state.

---

### 4. Critical Thresholds
| Parameter | Threshold | Consequence of Deviation |
| :--- | :--- | :--- |
| **Max Lipid Load** | $2.5 \times$ solids | Structural lattice collapse / leakage. |
| **Moisture Limit** | $\le 2.0\%$ | Loss of glassy state; premature oxidation. |
| **Cation Ratio** | $0.05 : 1$ | Emulsion break during dehydration phase. |
