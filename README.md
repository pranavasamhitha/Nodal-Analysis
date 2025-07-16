# Nodal-Analysis
## Gas Well Nodal Analysis using Python (IPR–TPR Curves)

This project demonstrates a practical **Nodal Analysis for a gas well**, implemented using Python. Real-world data from **PetroWiki** has been used to model:

- **Inflow Performance Relationship (IPR)** – representing the reservoir’s deliverability.
- **Tubing Performance Relationship (TPR)** – capturing the pressure drop required to lift gas through different tubing sizes.

The main objective is to compute and visualize the **Operating Point**, where IPR and TPR intersect, indicating the well’s actual stable flow rate and bottomhole flowing pressure under current reservoir and tubing conditions.


## Concept Overview

###  Inflow Performance Relationship (IPR)
- Illustrates how much gas the **reservoir can supply** to the wellbore.
- Plots **bottomhole flowing pressure (Pwf)** versus **flow rate (Q)**.
- Affected by reservoir pressure, permeability, and fluid properties.

###  Tubing Performance Relationship (TPR)
- Represents the **pressure required** to lift gas through the tubing to surface.
- Each tubing size (1.90", 2.375", and 2.875") has a unique pressure-flow behavior due to **frictional and accelerational losses**.
- TPR curves are plotted as **flow rate (Q)** vs **bottomhole pressure (Pwf)**.


##  Project Workflow

1. **Imported IPR data** from PetroWiki — tabulated values of flow rate vs bottomhole pressure.
2. **Defined TPR data** for 3 tubing diameters to capture lift performance behavior.
3. Used **interpolation** to generate smooth, continuous IPR and TPR curves.
4. Employed Python's `fsolve` function to compute **intersection points** (operating points) between IPR and each TPR curve.
5. Visualized results using **Matplotlib**, showing:
   - Reservoir deliverability (IPR)
   - Tubing performance (TPR)
   - Computed operating point for each tubing size



## Visual Output

The plot includes:
- **Green IPR Curve** – how much gas the reservoir can supply.
- **Red, Blue, and Purple TPR Curves** – pressure required for different tubing sizes.
- **Operating Points** – highlighted at the intersection of IPR and each TPR, indicating:
  - Flow Rate (Mscf/day)
  - Pwf (psi)


## Significance

- Helps assess whether the gas well can **flow naturally** or needs assistance (e.g., compression).
- Aids in **selecting optimal tubing diameter** for efficient gas lift.
- Supports reservoir and production engineers in making **informed design and operational decisions**.
- Enhances understanding of **well performance dynamics** under varying tubing conditions.

- Libraries used:
  - `numpy` – numerical operations
  - `pandas` – handling tabular IPR and TPR data
  - `matplotlib` – plotting curves and visualizing results
  - `scipy.optimize.fsolve` – numerical intersection point calculation
  - `scipy.interpolate.interp1d` – generating smooth curves from data




