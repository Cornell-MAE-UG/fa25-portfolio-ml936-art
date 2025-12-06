---
layout: project
title: Crane Design, Part 2
description: Assumption of Non Rigid Crane Arms
technologies: [Autodesk, Illustrator]
image: /assets/images/crane-design-step2.png
---


## Step 2 — Flexible Beam Analysis (Bar Treated as a Beam)

In this step, the bar is no longer modeled as a rigid link. Instead, it behaves as a cantilever beam subject to bending under two transverse forces:  
(1) the payload applied at the free end of the beam, and  
(2) the vertical component of the actuator force applied at an interior point located 0.40 m from the fixed end.  
The objective is to verify that the beam deflection stays within 2% of its length and to select a beam cross-section that satisfies this constraint with minimal material.

---

### **Problem Definition and Assumptions**

- The beam length is **L = 1.2 m**.  
- Fixed support at **Pin A**; free end at the payload location.  
- The actuator pin is located at **x = 0.40 m** from the fixed end.  
- Only vertical components of forces contribute to bending.  
- Material is structural steel with **E = 200×10⁹ Pa**.  
- Forces considered:
  - Payload force **W** (N) at the tip.  
  - Actuator vertical component **F_a** (N) at 0.40 m.

These assumptions simplify the analysis to a standard cantilever-beam deflection problem.

### **Transverse Load Model**

The combined vertical deflection at the free end can be expressed in compact form as:
δ_max = (0.576·W + 0.0853·F_a) / (E·I)

where  
- δ_max = maximum vertical deflection (m)  
- W = payload (N)  
- F_a = actuator vertical component (N)  
- E = Young’s modulus (Pa)  
- I = second moment of area of the beam (m^4)

This expression is derived by superposing the standard deflection formulas for:  
(1) a tip load, and  
(2) a point load at an intermediate position.

### **Deflection Constraint**

The design requirement limits beam deflection to **2% of its total length**:
δ_allow = 0.02 · L
With L = 1.2 m:
δ_allow = 0.024 m
This is the maximum deflection allowed under the worst-case loading condition.

### **Required Beam Stiffness (Solve for I)**
Rearranging the deflection equation to determine the required moment of inertia:
I_req = (0.576·W + 0.0853·F_a) / (E · δ_allow)
Using the full-load design case for the mechanism yields:
I_req ≈ 3.6×10^-7 m^4
Any beam with **I ≥ I_req** satisfies the 2% deflection requirement.

### **Final Beam Selection**

To keep mass low while satisfying stiffness requirements, a **50×50×6.5 mm square steel tube** is selected.  
It provides:

- A moment of inertia greater than **3.6×10⁻⁷ m⁴**,  
- A deflection less than **2% of the beam length**,  
- Roughly **45% less material** than a solid square bar of the same outer size.

This makes it a structurally efficient and manufacturable choice for the final design.


