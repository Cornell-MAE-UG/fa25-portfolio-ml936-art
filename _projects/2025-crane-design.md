---
layout: project
title: Crane Design
description: Design of simple crane that maximizes lifting capacity
technologies: [Autodesk Fusion]
image: /assets/images/2025-crane-design.png
---

Rigid-Bar Mechanism
(a) Problem, Constraints, Objectives, DOF
Problem.
Design a compact 2D lifting mechanism that fits inside a 150 cm × 50 cm design envelope and uses:
•	one straight bar (single rigid link),
•	three pin supports (two on ground, one moving),
•	one catalog linear actuator.
The goal is to lift the heaviest possible payload to the highest possible vertical position while staying within actuator force limits and the geometric envelope.
Key constraints
•	Bar must stay within a 1.5 m (x-direction) by 0.5 m (y-direction) box.
•	Exactly three pin joints:
o	A and B fixed to the ground,
o	C sliding on the bar.
•	Actuator must be picked from the Tolomatic online catalog (only maximum force rating used).
•	All supports and actuator are treated as rigid in Step 1.
Design choice (geometry).
•	Bar length: L=1.2 m
•	Ground pin at bar root: A=(0, 0)
•	Ground pin for actuator: B=(0, 0.50)
•	Moving pin on the bar: C located 0.40 m from A along the bar
•	Payload at bar tip: D at 1.20 m from A
In the initial “down” position the bar is horizontal; in the final “up” position it has rotated about 21°, lifting the payload approximately 0.5 m (within the 50 cm height limit).
Degrees of freedom
With two ground pins (A, B), one moving pin (C) and a single actuator, the mechanism has one degree of freedom: the rotation of the bar about A. Actuator stroke uniquely sets the bar angle and therefore the payload height.
________________________________________
(c) Mechanism Illustration 
