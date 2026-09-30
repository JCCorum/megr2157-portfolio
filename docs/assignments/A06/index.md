# A6 – Parametric Bracket Model and Engineering Drawing

## Objective

The objective of this assignment was to continue the bracket design developed in Assignment A5 by converting the bracket into a fully parametric SOLIDWORKS model and creating a fully dimensioned third-angle multiview engineering drawing.

The parametric model was driven by the strength-analysis equations and geometric relationships developed during A5. The final engineering drawing included functional dimensions, engineered sliding-fit tolerances, general tolerances, centerlines, center marks, material information, and a completed title block.

---

## Previous Design Basis

The A6 bracket was based on the final design developed during Assignment A5.

The selected design conditions were:

- Material: ASTM A36 Steel
- Applied strap load: 795 lbf per side
- Safety factor: 4
- Yield strength: approximately 36.259 ksi
- Elastic modulus: approximately 29.008 × 10^6 psi
- Maximum allowable deflection: 0.005 in

The bracket was divided into five structural features:

- Feature A – circular cantilever strap support
- Feature B – axially loaded rectangular member
- Feature C – simply supported rectangular beam
- Feature D – two symmetric axial support members
- Feature E – two symmetric upper cantilever members

The dimensions developed during A5 were used as the starting point for the A6 parametric model.

---

## Parametric Design

### Global Variables and Equations

The bracket was rebuilt using SOLIDWORKS global variables and equations so that the geometry could update automatically when a governing value changed.

The primary input parameters included:

- `F_load`
- `SF`
- `Yield Strength`
- `E`
- `max deflection`
- `a`
- `b`
- `c`
- `L_A`

Additional calculated variables were created for the dimensions of Features A through E.

![Global variables and equations 1](images/a6-equations-1.jpg)

*Figure 1. First section of the SOLIDWORKS global-variable and equation table.*

![Global variables and equations 2](images/a6-equations-2.jpg)

*Figure 2. Second section of the SOLIDWORKS global-variable and equation table.*

![Global variables and equations 3](images/a6-equations-3.jpg)

*Figure 3. Final section of the SOLIDWORKS global-variable and equation table.*

### Analytical Equation Used to Drive the Model

One of the primary analytically controlled dimensions was the radius of Feature A.

From the A5 bending-stress analysis,

\[
r_A =
\left(
\frac{4(SF)(F_{load})(L_A)}
{\pi \sigma_{yield}}
\right)^{1/3}
\]

This relationship was entered directly into the SOLIDWORKS equation manager rather than calculating the value separately and manually entering the resulting dimension.

The diameter of Feature A was then defined parametrically as:

\[
D_A = 2r_A
\]

As a result, changing the applied load, safety factor, material yield strength, or Feature A length causes the Feature A diameter to update automatically.

---

## Parametric Feature Geometry

### Feature A

Feature A was parameterized using the calculated diameter and the selected axial length.

Final nominal dimensions included:

- Diameter: approximately 0.875 in
- Axial length: 0.750 in

![Feature A parametric dimensions](images/a6-feature-a.jpg)

*Figure 4. Parametric dimensions controlling Feature A.*

---

### Feature B

Feature B was related directly to Feature A.

The width of Feature B was defined from the diameter of Feature A, while the height and thickness were controlled by the relationships developed during A5.

Final nominal dimensions included:

- Width: approximately 0.875 in
- Height: approximately 1.313 in
- Thickness: approximately 0.200 in

![Feature B parametric dimensions](images/a6-feature-b.jpg)

*Figure 5. Parametric dimensions controlling Feature B.*

---

### Feature C

Feature C was modeled from the support geometry and the stress-governed thickness obtained during A5.

Final nominal dimensions included:

- Overall length: approximately 3.5 in
- Depth: approximately 0.950 in
- Thickness: approximately 0.911 in

![Feature C parametric dimensions](images/a6-feature-c.jpg)

*Figure 6. Parametric dimensions controlling Feature C.*

---

### Feature D

The two Feature D members were modeled symmetrically.

The width of each support was retained as approximately 0.498 in because the assumed geometric value exceeded the minimum dimension required by the A5 stress analysis.

The Feature D length was tied to the vertical fit dimension required by the rigid T-beam.

![Feature D parametric dimensions](images/a6-feature-d.jpg)

*Figure 7. Parametric dimensions controlling the symmetric Feature D members.*

---

### Feature E

The two Feature E members were also modeled symmetrically.

Final nominal dimensions included:

- Height: approximately 0.744 in
- Cantilever length determined by the required T-beam clearance
- Depth inherited from the Feature C geometry

![Feature E parametric dimensions](images/a6-feature-e.jpg)

*Figure 8. Parametric dimensions controlling the symmetric Feature E members.*

---

## Sliding-Fit Geometry

The assignment required three different sliding fits between the bracket and the rigid T-beam.

Separate global variables were created for the three functional gaps:

- `Gap_a`
- `Gap_b`
- `Gap_c`

The nominal dimensions used in the final model were:

| Fit Dimension | Nominal Size | Drawing Tolerance |
| --- | ---: | ---: |
| Gap A | 0.5000 in | +0.0016 / -0.0000 in |
| Gap B | 1.0000 in | +0.0008 / -0.0000 in |
| Gap C | 1.5000 in | +0.0016 / -0.0000 in |

These dimensions were parameterized independently from the original T-beam dimensions so that the bracket geometry represents the required clearances rather than simply reproducing the nominal rigid-body dimensions.

![Parameterized fit dimensions](images/a6-fit-parameters.jpg)

*Figure 9. Parametric dimensions controlling the three sliding-fit interfaces.*

---

## Completed Parametric Model

After all governing dimensions and fit clearances were connected to the global variables, the model was rebuilt to verify that the equations and geometric relationships remained valid.

![Completed parametric bracket](images/a6-final-model.jpg)

*Figure 10. Completed parametric SOLIDWORKS bracket model.*

---

## Engineering Drawing

A third-angle multiview engineering drawing was created from the completed parametric model.

The drawing includes:

- Front view
- Top view
- Right-side view
- Isometric view
- Centerlines and center marks
- Functional and structural dimensions
- Three engineered sliding-fit tolerances
- General tolerance block
- ASTM A36 Steel material designation
- Drawing title, name, date, drawing number, and scale

The Front view was selected as the primary view because it displays the largest number of structural features and most clearly communicates the overall bracket geometry.

![Completed engineering drawing](images/a6-final-drawing.jpg)

*Figure 11. Completed third-angle multiview engineering drawing.*

---

## Dimension and Tolerance Strategy

The drawing dimensions were separated into three primary functional categories.

### Class 3 – Explicit Fit Dimensions

The three T-beam sliding-fit dimensions received individual unilateral tolerance callouts and were displayed to four decimal places.

Examples include:

- Gap A: 0.5000 +0.0016 / -0.0000 in
- Gap B: 1.0000 +0.0008 / -0.0000 in
- Gap C: 1.5000 +0.0016 / -0.0000 in

### Class 2 – Functional Dimensions

Dimensions that influence structural strength, stiffness, or functional alignment were assigned tighter precision through the drawing tolerance block.

Structural dimensions were generally displayed to three decimal places, corresponding to:

\[
X.XXX \pm 0.005
\]

Functional location dimensions were displayed to two decimal places, corresponding to:

\[
X.XX \pm 0.01
\]

### Class 1 – Non-Critical Dimensions

Dimensions that primarily define the overall envelope of the part without controlling a critical fit or structural requirement were displayed to one decimal place:

\[
X.X \pm 0.02
\]

This prevented unnecessarily tight manufacturing tolerances from being applied to non-critical geometry.

---

## Drawing Tolerance Block

The completed drawing used the following general tolerance convention:

- X.X ± 0.02 in
- X.XX ± 0.01 in
- X.XXX ± 0.005 in

Dimensions with individually specified tolerances, such as the three sliding-fit dimensions, override the general tolerance block.

---

## Design Changes and Mistakes

During the parametric modeling process, several geometric relationships initially relied on fixed dimensions from the A5 model. These values had to be replaced with global-variable relationships so that changes to governing parameters would propagate through the bracket.

One example occurred when the dimensions corresponding to the rigid T-beam were initially tied directly to the original `a`, `b`, and `c` values. The assignment required actual sliding clearances, so separate `Gap_a`, `Gap_b`, and `Gap_c` parameters were later created. The dependent equations for Features C, D, and E were then updated to reference the new gap parameters.

Another issue involved the relationship between Feature A and Feature B. Feature B was originally created using converted geometry. The final model was revised so that its geometry remained linked to the calculated Feature A diameter through parametric relationships.

[Add any other mistake you want to document here.]

---

## Lessons Learned

### Parametric Equation Control

A major lesson from the parametric portion of the assignment was the difference between entering a previously calculated numerical value and embedding the analytical relationship directly into the CAD model.

Feature A provided a clear example. Its diameter was not entered manually as 0.875 in. Instead, the radius was calculated inside SOLIDWORKS using the A5 bending-stress equation, and the diameter was defined as twice that radius.

Because downstream dimensions referenced the Feature A diameter, a change to an upstream design variable could propagate through multiple later features automatically.

When the T-beam fit geometry was later changed from the original `a`, `b`, and `c` dimensions to the explicit `Gap_a`, `Gap_b`, and `Gap_c` parameters, some dependent equations had to be updated manually. Once those references were corrected, the associated model dimensions rebuilt automatically.

### Functional Versus Non-Functional Tolerances

The drawing process demonstrated that not every dimension should receive the same manufacturing tolerance.

For example, the Feature C thickness was displayed as a three-decimal dimension:

\[
0.911
\]

Under the drawing tolerance block this corresponds to:

\[
\pm0.005\text{ in}
\]

Feature C thickness is structurally functional because it was determined from the bending-stress analysis and directly affects the strength of the bracket.

In contrast, the Feature C overall length was displayed as:

\[
3.5
\]

which corresponds to the looser:

\[
\pm0.02\text{ in}
\]

general tolerance. The overall length is needed to define the part envelope, but small variation in that dimension does not directly control one of the sliding fits or the governing structural thickness.

Holding a non-critical dimension to an unnecessarily tight tolerance would increase manufacturing difficulty and potentially increase manufacturing cost without producing a meaningful functional benefit.

### Sliding-Fit Tolerances

The three interfaces with the rigid T-beam required special treatment because the bracket must slide over the mating geometry.

Rather than relying on the general tolerance block, each fit dimension received its own unilateral tolerance. This allows the bracket opening to remain at or above the required nominal clearance while preventing an undersized opening from interfering with assembly.

### Drawing Organization

The multiview drawing also demonstrated the importance of dimension placement. Dimensions were reorganized so that local dimensions remained close to the associated features while larger-span dimensions were placed farther from the object.

Redundant dimensions were removed to reduce conflicting tolerance chains and improve readability.

---

## Assignment Time

Actual time spent:

**[ENTER TOTAL TIME]**

Approximate breakdown:

- Reviewing assignment and references: [time]
- Parametric equation setup: [time]
- Revising and troubleshooting CAD relationships: [time]
- Engineering drawing and tolerancing: [time]
- Portfolio documentation: [time]

---

## CAD and Drawing Files

[Download the completed A6 SOLIDWORKS part](files/A6-Bracket.SLDPRT)

[Download the completed A6 SOLIDWORKS drawing](files/A6-Bracket.SLDDRW)

[Download the completed A6 engineering drawing PDF](files/A6-Bracket-Drawing.pdf)

---

## References

Machinery’s Handbook, 32nd ed., *Standard Drafting Practices*, pp. 621–635.

MEGR 2156 Assignment A6 instructions and supplied bracket/T-beam specifications.

MEGR 2156 Assignment A5 analytical bracket design calculations.
