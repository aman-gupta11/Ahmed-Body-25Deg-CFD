# Ahmed Body (25° Slant) CFD Validation — OpenFOAM

Steady RANS simulation of the Ahmed bluff body at 25° slant, validated against published experimental data.

## Mesh

- Type: snappyHexMesh
- Cell count: 2,223,114

## Result

| | This work | Reference | Error |
|---|---|---|---|
| Cd | 0.301 | 0.299 | +0.7% |
Cd matches within 1%.

## Setup

- **Solver:** simpleFoam, k-ω SST
- **Mesh:** snappyHexMesh, ~2.2M cells, 5 boundary layers on body
- **Flow:** U = 40 m/s, Re ≈ 2.78×10⁶, L = 1.044 m, A = 0.112 m²
- **OpenFOAM:** ESI v2406
- **Geometry:** modeled in Ansys Discovery, exported OBJ.
- **Case base:** adapted from the OpenFOAM `motorBike` tutorial; geometry, domain, mesh refinement, solver settings and force setup modified for this case

## References

- **Geometry & background:** Ahmed, Ramm, Faltin (1984), SAE 840300
- **Validation target (Cd, Cl):** Lienhart, Becker (2003), SAE 2003-01-0656
- **Wake velocity data:** ERCOFTAC Case 082 (LDA measurements, hosted dataset of Lienhart & Becker)


