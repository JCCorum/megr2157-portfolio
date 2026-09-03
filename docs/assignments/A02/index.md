# A2 – Truss Stress Analysis

## Objective:

## Design Requirements and Known Parameters:

## Analyze

### Truss Geometry:
The planar truss geometry was designed using the given dimensions of a = 0.4 m and b = 0.3 m. Seven members and five joints were selected to produce a statically determinate planar truss satisfying m + r = 2j. The complete geometry, assumptions, support-reaction analysis, and initial joint free-body diagrams are shown below.

![Planar truss schematic, assumptions, support reactions, and initial joint FBDs](images/truss-analysis-front.jpg)

*Figure 1. Initial planar truss geometry, determinacy check, support reactions, and free-body diagrams for Joints A and B.*

### Support Reactions:

The external support reactions were found before method of joints was used. Horizontal sum of forces produced a zero horizontal reaction at A, while vertical sum of forces and sum of moments about joint A were used to identify the vertical reactions at A and B. The symbolic work and corresponding whole-truss free-body diagram are included in Figure 1.

### Joint Free Body Diagrams:

A free-body diagram corresponding to each joint was drawn so that the internal axial forces could be found with method of joints. Member-force directions were established from the tension or compression behavior of the corresponding members and resolved using the defined positive x- and y-coordinate directions. The diagrams for Joints A and B are shown in Figure 1, while the remaining joints are shown in Figure 2.

### Symbolic Member-Force Analysis:

Method of joints was used to determine the internal member forces symbolically before numerical substitution. The diagonal member lengths were represented by d and e so that the equilibrium equations could be maintained in symbolic form. Figure 2 shows the remaining joint FBDs and the symbolic relationships used to determine the member forces.

![Symbolic and numerical method-of-joints calculations](images/truss-analysis-back.jpg)

*Figure 2. Free-body diagrams for Joints C, D, and E with symbolic and numerical member-force calculations.*

### Numerical Member-Force Analysis:

The given dimensions and a chosen load of P = 25 kN were substituted into the symbolic relationships. The resulting internal forces were classified as tension, compression, or zero-force based on their directions. The complete numerical calculations are shown in Figure 2.

### Critical Member Identification:

The largest internal-force magnitude occurred in members CE and DE. Both members carried approximately 20.03 kN, with CE in compression and DE in tension. This force magnitude was therefore used to determine the minimum common cross-sectional area for all truss members.

### Truss Member Cross-Section Design:

#### Knowns and Unknowns:

The largest internal force, required safety factor, and A500 Grade C steel properties were used to size the common member cross-section. Normal stress was compared with the allowable yield stress after application of the required safety factor of 3.5. The symbolic derivation, numerical minimum area, approximate truss weight, and selected rectangular proportion are shown below.

![Member cross-section and truss weight calculations](images/member-sizing.jpg)

*Figure 3. Minimum truss-member cross-sectional area and approximate planar-truss weight calculations.*
#### Symbolic Solution:

The symbolic normal-stress derivation is shown in Figure 3.

#### Numerical Solution:

The resulting theoretical minimum member area was approximately **203.21 mm²** using A500 Grade C steel.

#### Estimated Truss Weight:

Using the theoretical minimum area and total member length, the analytical truss weight was estimated as approximately **51.97 N**.

### Pin Design:

#### Knowns and Unknowns:

#### Critical Pin FBD:

The shear-force resultants were evaluated at each pin before sizing the common pin cross-section. Pins C and D were found to carry the largest resultant shear force, with a magnitude of 25 kN, and therefore control the identical-pin design. The individual pin-force analyses are shown below.

![Pin shear-force comparison](images/pin-force-analysis.jpg)

*Figure 4. Resultant shear-force analysis for Pins A through E used to identify the critical pin connection.*

#### Symbolic Single-Shear Analysis:

The required pin area was determined using the maximum 25 kN shear force, the hardened-tool-steel shear yield strength, and the required safety factor of 4. Because the problem specifies a single-shear connection, one shear plane was used in the stress calculation. The symbolic and numerical calculations are shown below.

![Critical pin sizing and weight calculations](images/pin-sizing.jpg)

*Figure 5. Critical single-shear pin sizing, minimum diameter, selected pin length, and estimated combined pin weight.*

#### Numerical Pin Size:

The minimum calculated pin area was approximately **85.32 mm²**, corresponding to a minimum cylindrical diameter of approximately **10.42 mm**.

#### Estimated Pin Weight:

The identical pins were sized using the calculated minimum cross-section and a common length based on the member stack at the joints. The approximate combined weight calculation for the five pins is included in Figure 5.

## Decide:
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

### Geometry Selection:

### Member Cross-Section Selection:

### Pin Size Selection:

## Communicate:

### CAD Model:

The completed planar truss geometry was modeled in SOLIDWORKS as a single part in accordance with the assignment instructions and Appendix B. The analytical member dimensions were transferred into the CAD geometry while maintaining the required common cross-sectional area through the truss members and joint regions. The current completed truss model is shown below.

![SOLIDWORKS planar truss model](images/truss-cad-model.png)

*Figure 6. Completed SOLIDWORKS model of the planar truss.*

The truss body was completed within the available assignment time. Additional CAD development of the individual pins was not completed before submission.

### CAD Mass Properties:

### Analytical and CAD Weight Comparison:

### CAD File Download:

The available SOLIDWORKS CAD file for the planar truss can be downloaded below.

[**Download A2 Planar Truss SOLIDWORKS Part**](files/A2_Truss.SLDPRT)

## Mistakes and Design Iterations:

## Engineering Lessons Learned:

## Assignment Time:

This assignment took me approximately 18 hours.
