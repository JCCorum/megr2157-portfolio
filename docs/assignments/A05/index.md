# A5 – Bracket Design:

## Objective:

The objective of this assignment was to design a structural bracket using fundamental strength-of-materials methods. Five structural features were individually modeled using appropriate normal-stress, bending-stress, and deflection relationships. Each feature was sized independently for stress and stiffness, after which the governing dimensions were used to define the final bracket geometry.

## Design Requirements and Selected Parameters:

The bracket was required to support two symmetric polyester-strap loads using a safety factor of 4 while limiting the deflection of each analyzed feature to 0.005 in. Failure due to direct shear stress and shear deformation were neglected as specified by the assignment.

The selected load was:

**F<sub>load</sub> = 795 lbf**

ASTM A36 steel was selected as the bracket material.

Selected material and design properties:

- Elastic modulus: **E = 29.00755 × 10<sup>6</sup> psi**
- Yield strength: **σ<sub>yield</sub> = 36.25943 ksi**
- Density: **ρ = 0.2836 lb/in<sup>3</sup>**
- Safety factor: **SF = 4**
- Allowable normal/bending stress: **σ<sub>allow</sub> = σ<sub>yield</sub>/SF ≈ 9.06486 ksi**
- Maximum allowable deflection per feature: **δ<sub>max</sub> = 0.005 in**

![Design requirements and initial design decisions](images/design-overview.jpg)

*Figure 1. Initial design constraints, material options, strap properties, and design assumptions.*

## Concept Geometry and Load Workflow:

The supplied bracket concept was divided into five structural features labeled A through E. Reactions calculated for one feature were carried forward as applied loads for subsequent features, producing the approximate load workflow:

**A → B → C → D → E**

Feature A was modeled as a cantilever with a circular cross-section, Feature B as an axially loaded rectangular bar, Feature C as a simply supported beam with a concentrated center load, Feature D as two symmetric axially loaded supports, and Feature E as two symmetric cantilever members.

## Material and Load Selection:

A near-maximum permitted load of **F<sub>load</sub> = 795 lbf** was selected so that the bracket would be designed near the upper end of the specified loading range of 500 lbf < F < 800 lbf.

ASTM A36 steel was selected from the three available materials. Although Ti-6Al-4V provided a substantially greater yield strength, ASTM A36 steel had the greatest elastic modulus of the available materials. Since the stiffness and deflection constraints were initially expected to be restrictive, the higher elastic modulus of ASTM A36 steel was considered advantageous.

## Stress and Stiffness Analysis:

### Feature A – Strap Support:

Feature A supports the polyester strap and was modeled as a circular cantilever subjected to a uniformly distributed load. The two 795 lbf strap loads produce a total equivalent load of:

**W<sub>A</sub> = 2F<sub>load</sub> = 1590 lbf**

over an assumed effective feature length of:

**L<sub>A</sub> = 0.750 in**

#### Feature A Stress Analysis:

The allowable bending stress was based on the ASTM A36 yield strength divided by the required safety factor. The bending-stress analysis produced:

**r<sub>A</sub>[σ<sub>max,allow</sub>] ≈ 0.43751 in**

#### Feature A Stiffness Analysis:

Using the cantilever-beam deflection relationship and the 0.005 in maximum-deflection constraint, the stiffness analysis produced:

**r<sub>A</sub>[δ<sub>max</sub>] ≈ 0.16471 in**

#### Feature A Design Result:

Because the stress requirement was larger than the stiffness requirement, stress governed the design of Feature A.

**r<sub>A,min</sub> ≈ 0.43751 in**

**Ø<sub>A,min</sub> = 2r<sub>A,min</sub> ≈ 0.87502 in**

![Feature A stress analysis](images/feature-a-stress.jpg)

*Figure 2. Feature A assumptions, free-body diagram, and bending-stress analysis.*

### Feature B – Axially Loaded Member:

Feature B was modeled as a purely axially loaded rectangular member. Its width was assumed equal to the calculated diameter of Feature A:

**w<sub>B</sub> = Ø<sub>A</sub>**

Its axial height was initially assumed to equal:

**h<sub>B</sub> = L<sub>B</sub> = 1.5Ø<sub>A</sub>**

The remaining thickness, **t<sub>B</sub>**, was treated as the design variable.

The axial load transferred from Feature A was:

**F<sub>B</sub> = R<sub>AB</sub> = 2F<sub>load</sub> = 1590 lbf**

#### Feature B Stress Analysis:

The axial-stress analysis produced:

**t<sub>B</sub>[σ<sub>max</sub>] ≈ 0.20046 in**

#### Feature B Stiffness Analysis:

The axial-deformation analysis produced:

**t<sub>B</sub>[δ<sub>max</sub>] ≈ 0.01644 in**

#### Feature B Design Result:

Stress governed Feature B.

**t<sub>B,min</sub> ≈ 0.20046 in**

![Feature A stiffness and Feature B analysis](images/feature-a-b-design.jpg)

*Figure 3. Feature A stiffness calculation and both the axial-stress and stiffness analyses for Feature B.*

### Feature C – Simply Supported Beam:

Feature C was modeled as a simply supported rectangular beam with the reaction from Feature B applied as a concentrated load at its center:

**F<sub>C</sub> = |R<sub>BC</sub>| = 1590 lbf**

The two Feature D members were modeled as symmetric simple supports. Therefore:

**|R<sub>CD</sub>| = F<sub>C</sub>/2 = 795 lbf**

The effective support-to-support span was defined as:

**L<sub>C</sub> = 2a + 2b = 2.9944 in**

The overall physical length of Feature C was defined as:

**l<sub>C</sub> = 3a + 2b = 3.4924 in**

The width of Feature C was defined from the preceding feature geometry as:

**w<sub>C</sub> = L<sub>A</sub> + t<sub>B,min</sub> = 0.95046 in**

The thickness **t<sub>C</sub>** was treated as the design variable.

#### Feature C Stress Analysis:

The bending-stress analysis produced:

**t<sub>C</sub>[σ<sub>max</sub>] ≈ 0.91044 in**

#### Feature C Stiffness Analysis:

The simply-supported-beam deflection analysis produced:

**t<sub>C</sub>[δ<sub>max</sub>] ≈ 0.42620 in**

#### Feature C Design Result:

Stress governed Feature C.

**t<sub>C,min</sub> ≈ 0.91044 in**

![Feature C analysis](images/feature-c-design.jpg)

*Figure 4. Feature C geometry assumptions, free-body diagram, and stress and stiffness analyses.*

### Feature D – Axially Loaded Supports:

The two Feature D members were modeled symmetrically as axially loaded rectangular members. Each Feature D carries one half of the Feature C load:

**F<sub>D</sub> = |R<sub>CD</sub>| = 795 lbf**

The axial length of Feature D was defined by the T-beam dimension:

**L<sub>D</sub> = h<sub>D</sub> = c = 1.499 in**

The into-page length was assumed equal to the width of Feature C:

**l<sub>D</sub> = w<sub>C</sub> = 0.95046 in**

The width **w<sub>D</sub>** was treated as the analytical design variable to determine whether the preliminary geometry-based value:

**w<sub>D</sub> = a = 0.498 in**

was sufficient.

#### Feature D Stress Analysis:

The axial-stress analysis produced:

**w<sub>D</sub>[σ<sub>max</sub>] ≈ 0.09227 in**

#### Feature D Stiffness Analysis:

The axial-deformation analysis produced:

**w<sub>D</sub>[δ<sub>max</sub>] ≈ 0.00865 in**

#### Feature D Design Result:

Although stress governed the analytical requirement, both calculated minimum dimensions were substantially smaller than the geometry-based value of 0.498 in. Therefore, the assumed geometry was retained:

**w<sub>D</sub> = a = 0.498 in**

![Feature D analysis](images/feature-d-design.jpg)

*Figure 5. Feature D assumptions, free-body diagram, and axial-stress and stiffness analyses.*

### Feature E – Upper Cantilever Supports:

The two Feature E members were modeled symmetrically as rectangular cantilevers fixed at the D-E connection. Each Feature E carries a load of:

**F<sub>E</sub> = |R<sub>DE</sub>| = 795 lbf**

A conservative concentrated free-end load was used in place of the distributed bearing load because the exact load distribution between Feature E and the rigid T-beam was uncertain.

The effective unsupported cantilever length was:

**L<sub>E</sub> = b = 0.9992 in**

The into-page length was assumed equal to the Feature D length and Feature C width:

**l<sub>E</sub> = l<sub>D</sub> = w<sub>C</sub> = 0.95046 in**

The height **h<sub>E</sub>** was treated as the design variable.

#### Feature E Stress Analysis:

The conservative point-load bending-stress analysis produced:

**h<sub>E</sub>[σ<sub>max</sub>] ≈ 0.74377 in**

#### Feature E Stiffness Analysis:

The corresponding cantilever-deflection analysis produced:

**h<sub>E</sub>[δ<sub>max</sub>] ≈ 0.28432 in**

#### Feature E Design Result:

Stress governed Feature E.

**h<sub>E,min</sub> ≈ 0.74377 in**

![Feature E analysis](images/feature-e-design.jpg)

*Figure 6. Feature E assumptions, cantilever free-body diagram, and stress and stiffness analyses.*

## Final Analytical Dimensions:

| Feature | Stress Requirement | Stiffness Requirement | Selected/Governing Dimension |
| --- | ---: | ---: | ---: |
| A | r<sub>A</sub>[σ<sub>max</sub>] = 0.43751 in | r<sub>A</sub>[δ<sub>max</sub>] = 0.16471 in | r<sub>A,min</sub> = 0.43751 in |
| B | t<sub>B</sub>[σ<sub>max</sub>] = 0.20046 in | t<sub>B</sub>[δ<sub>max</sub>] = 0.01644 in | t<sub>B,min</sub> = 0.20046 in |
| C | t<sub>C</sub>[σ<sub>max</sub>] = 0.91044 in | t<sub>C</sub>[δ<sub>max</sub>] = 0.42620 in | t<sub>C,min</sub> = 0.91044 in |
| D | w<sub>D</sub>[σ<sub>max</sub>] = 0.09227 in | w<sub>D</sub>[δ<sub>max</sub>] = 0.00865 in | w<sub>D</sub> = a = 0.498 in |
| E | h<sub>E</sub>[σ<sub>max</sub>] = 0.74377 in | h<sub>E</sub>[δ<sub>max</sub>] = 0.28432 in | h<sub>E,min</sub> = 0.74377 in |

Stress governed Features A, B, C, and E under the selected analytical models. Feature D was also stress-governed analytically, but its selected width was instead controlled by the assumed bracket geometry.

## CAD Model:

The final bracket geometry was modeled in SOLIDWORKS using the dimensions obtained from the stress and stiffness analyses of Features A through E. The completed model reflects the final selected feature sizes used for the bracket design.

![Completed SOLIDWORKS bracket model](images/bracket.jpg)

*Figure 7. Completed SOLIDWORKS model of the designed bracket.*

### CAD File Download:

[Download the completed SOLIDWORKS bracket file](files/Bracket.SLDPRT)

## Mistakes and Design Iterations:

Several modeling assumptions were revised during the design process. The effective support locations for Feature C were initially uncertain until the two Feature D members were modeled as symmetric simple supports and the effective span, L<sub>C</sub>, was defined between their centroids. Feature D was initially assigned a width of a = 0.498 in before analysis; the subsequent stress and stiffness calculations confirmed that this assumed width exceeded both analytical minimum requirements.

The loading model for Feature E was also revised. The rigid T-beam contact was initially considered as a uniformly distributed bearing load. Because the exact bearing distribution was uncertain, a more conservative concentrated free-end load was ultimately used for the stress and stiffness calculations.

## Lessons Learned:

### Governing Failure Mode:

Feature C provides a clear comparison between stress- and stiffness-controlled sizing. The stress analysis required:

**t<sub>C</sub>[σ<sub>max</sub>] ≈ 0.91044 in**

while the stiffness analysis required:

**t<sub>C</sub>[δ<sub>max</sub>] ≈ 0.42620 in**

Stress therefore governed the final Feature C thickness by approximately:

**0.91044 - 0.42620 = 0.48424 in**

### Error Propagation:

The geometry of later features depended directly on dimensions calculated earlier in the design process. For example, the Feature A diameter, Ø<sub>A</sub>, was used to establish the width and height of Feature B. The governing Feature B thickness, t<sub>B,min</sub>, was then used with L<sub>A</sub> to determine the width of Feature C:

**w<sub>C</sub> = L<sub>A</sub> + t<sub>B,min</sub>**

Therefore, an error in an early calculation could propagate through several later feature dimensions. Carrying symbolic relationships forward before substituting numerical values helped make these dependencies easier to identify and check.

### Assumption Sensitivity:

Feature E demonstrated the sensitivity of the design to the assumed load distribution. A uniformly distributed bearing-load model initially produced a smaller required height, while modeling the same resultant force conservatively as a concentrated free-end load increased both the bending-stress and deflection requirements. The conservative point-load model was ultimately retained because the exact bearing distribution was uncertain.

## Assignment Time:

**Total time: 26 hours**

## References:

- *Machinery's Handbook*, 32nd Edition. Sections and tables used for simple stresses, bending stress, beam deflection, section modulus, and moments of inertia.
- Uline Heavy Duty Polyester Cord Strapping, Model S-12925.
- SOLIDWORKS Material Library, ASTM A36 Steel material properties.
