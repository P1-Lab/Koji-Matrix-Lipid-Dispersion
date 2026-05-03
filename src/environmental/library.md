### `src/environmental/`

This directory defines the atmospheric and moisture tolerance models required to maintain **Vitrification Grade** status during storage and transit. These files serve as the "environmental firewall" for the **FAT-OS**.

---

#### **moisture_tolerance.json**
*Critical thresholds for maintaining the glassy state ($T_g$).*

```json
{
  "model_id": "ENV-MOIST-01",
  "critical_limit": {
    "max_aw": 0.35,
    "target_moisture_pct": 2.0
  },
  "degradation_logic": {
    "0.36-0.45_aw": "Lattice plasticization; loss of brittle fracture properties",
    "0.46-0.60_aw": "Molecular mobility increase; lipid migration initiated",
    ">0.60_aw": "Total wall failure; oxidative compromise"
  },
  "verification": "Halogen Moisture Analysis"
}
```

---

#### **atmospheric_stability.json**
*Nitrogen-flush parameters for 24-month oxidative shielding.*

```json
{
  "model_id": "ENV-GAS-02",
  "gas_composition": {
    "N2": "99.0%",
    "O2_max": "1.0%",
    "CO2": "Trace"
  },
  "stability_metrics": {
    "shelf_life_months": 24,
    "max_peroxide_value": 1.0,
    "max_anisidine_value": 3.0
  },
  "packaging_requirement": "High-barrier metallized film (OTR < 0.1 cc/m2/day)"
}
```

---

#### **storage_logic.md**
*Technical guide for environmental lifecycle management.*

*   **Vitrification Maintenance:** The primary threat to **KMLD** integrity is moisture-induced plasticization. If the water activity ($a_w$) exceeds 0.35, the starch barrier transitions from a "glass" to a "rubber," leading to immediate lipid leakage.
*   **Oxidative Shielding:** Nitrogen flushing is mandatory to displace residual oxygen within the porous koji-scaffold. Without this displacement, the internal "Physical Walls" are vulnerable to rancidity despite the external starch seal.
*   **Transit Protocol:** Product must be maintained in a cool, dry environment. Thermal spikes above $45^\circ\text{C}$ during shipping may initiate "sweating" if the $T_g$ baseline was not accurately calibrated during the `src/matrices/` phase.
*   **Audit Requirement:** Every production lot must undergo an environmental stress test—exposure to $40^\circ\text{C}$ at $50\%$ RH for 48 hours—to verify lattice stability.
