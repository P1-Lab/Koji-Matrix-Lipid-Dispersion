### `src/thermal_profiles/`

This directory provides the standardized thermal release data used to program the specific behavior of the **FAT-OS** implementation. These profiles allow for the customization of lipid release based on the intended cooking application, ranging from slow-render "animal fat" mimicry to high-heat flash searing.

---

#### **standard_render.json**
*Default profile for versatile "animal-fat" mimicry and consistent flavor delivery.*

```json
{
  "profile_id": "TP-STD-01",
  "base_matrix": "KMLD-YAM-01",
  "thermal_triggers": [
    {
      "temp_celsius": 60,
      "state": "activation",
      "release_rate": "0.05mg/s",
      "description": "Initial wall softening; phase transition initiates."
    },
    {
      "temp_celsius": 105,
      "state": "peak_render",
      "release_rate": "0.85mg/s",
      "description": "Complete lattice collapse; standard sizzle performance."
    }
  ]
}
```

---

#### **high_sear_flash.json**
*Optimized for high-heat stability and rapid, explosive payload delivery.*

```json
{
  "profile_id": "TP-FLASH-02",
  "base_matrix": "KMLD-YAM-01",
  "thermal_triggers": [
    {
      "temp_celsius": 90,
      "state": "retention",
      "release_rate": "0.01mg/s",
      "description": "High-amylose barrier maintained for surface browning."
    },
    {
      "temp_celsius": 165,
      "state": "explosive_release",
      "release_rate": "2.50mg/s",
      "description": "Total vitrified wall failure; immediate lipid saturation."
    }
  ]
}
```

---

#### **profile_application.md**
*Technical integration and calibration notes.*

*   **Environmental Buffering:** The chitin/glucan scaffold within the koji-mushroom matrix acts as a thermal buffer, shielding the lipid from immediate heat exposure and elevating the effective smoke point.
*   **Curve Selection:** Selection of the profile is dependent on the target Glass Transition Temperature ($T_g$) established in the `src/matrices/` configuration.
*   **Precision Industrial Mapping:** These profiles are designed to be mapped directly to industrial oven or extruder temperature probes to ensure the "Physical Wall" fails exactly at the desired timestamp of the production cycle.
*   **Vitrification Consistency:** All curves assume a baseline moisture content of $\le 2.0\%$ to ensure the starch barrier operates within the glassy regime.
