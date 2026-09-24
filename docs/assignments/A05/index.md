# A5 – Bracket Design:

## Objective:

The objective of this assignment was to design a structural bracket using fundamental strength-of-materials methods. Five structural features were individually modeled using appropriate normal stress, bending stress, and deflection relationships. Each feature was sized independently for stress and stiffness, after which the governing dimensions were used to define the final bracket geometry.

## Design Requirements and Selected Parameters:

The bracket was required to support two symmetric polyester-strap loads using a safety factor of 4 while limiting the deflection of each analyzed feature to 0.005 in. Failure due to direct shear stress and shear deformation were neglected as specified by the assignment.

A near-maximum permitted load of 795 lbf was selected for each strap load. ASTM A36 steel was selected because its comparatively high elastic modulus was expected to be advantageous for the stiffness requirements of the bracket.

Selected material properties:

- Elastic modulus: 29.00755 × 10^6 psi
- Yield strength: 36.25943 ksi
- Density: 0.2836 lb/in³
- Safety factor: 4
- Allowable normal/bending stress: approximately 9.06486 ksi
- Maximum allowable deflection per feature: 0.005 in

![Design requirements and initial design decisions](images/design-overview.jpg)

*Figure 1. Initial design constraints, material options, strap properties, and design assumptions.*

## Concept Geometry and Load Workflow:

The supplied bracket concept was divided into five structural features labeled A through E. Reactions calculated for one feature were carried forward as applied loads for subsequent features, producing the approximate load workflow: A → B → C → D → E.

Feature A was modeled as a cantilever with a circular cross-section, Feature B as an axially loaded rectangular bar, Feature C as a simply supported beam with a concentrated center load, Feature D as two symmetric axially loaded supports, and Feature E as two symmetric cantilever members.

## Material and Load Selection:

## Stress and Stiffness Analysis:

### Feature A – Strap Support:

Feature A supports the polyester strap and was modeled as a circular cantilever subjected to a uniformly distributed load. The two 795 lbf strap loads produce a total equivalent load of 1590 lbf over an assumed effective length of 0.750 in.

#### Feature A Stress Analysis:

The allowable bending stress was based on the ASTM A36 yield strength divided by the required safety factor. The bending-stress analysis produced a minimum radius of approximately:

**rA,stress = 0.43751 in**

#### Feature A Stiffness Analysis:

Using the cantilever-beam deflection relationship and the 0.005 in maximum-deflection constraint, the stiffness analysis produced:

**rA,stiffness = 0.16471 in**

#### Feature A Design Result:

Because the stress requirement was larger than the stiffness requirement, stress governed the design of Feature A.

**Minimum Feature A radius = 0.43751 in**

**Minimum Feature A diameter = 0.87502 in**

![Feature A stress analysis](images/feature-a-stress.jpg)

*Figure 2. Feature A assumptions, free-body diagram, and bending-stress analysis.*

### Feature B – Axially Loaded Member:

Feature B was modeled as a purely axially loaded rectangular member. Its width was assumed equal to the calculated diameter of Feature A, while its height was assumed to equal 1.5 times the diameter of Feature A. The remaining thickness was determined from the stress and stiffness requirements.

#### Feature B Stress Analysis:

The axial-stress analysis produced:

**tB,stress = 0.20046 in**

#### Feature B Stiffness Analysis:

The axial-deformation analysis produced:

**tB,stiffness = 0.01644 in**

#### Feature B Design Result:

Stress governed Feature B.

**Minimum Feature B thickness = 0.20046 in**

![Feature A stiffness and Feature B analysis](images/feature-a-b-design.jpg)

*Figure 3. Feature A stiffness calculation and Feature B axial stress and stiffness analyses.*

### Feature C – Simply Supported Beam:

#### Feature C Stress Analysis:

#### Feature C Stiffness Analysis:

#### Feature C Design Result:

### Feature D – Axially Loaded Supports:

#### Feature D Stress Analysis:

#### Feature D Stiffness Analysis:

#### Feature D Design Result:

### Feature E – Upper Cantilever Supports:

#### Feature E Stress Analysis:

#### Feature E Stiffness Analysis:

#### Feature E Design Result:

## Final Analytical Dimensions:

## CAD Model:

### CAD File Download:

## Mistakes and Design Iterations:

## Lessons Learned:

### Governing Failure Mode:

### Error Propagation:

### Assumption Sensitivity:

## Assignment Time:

## References
