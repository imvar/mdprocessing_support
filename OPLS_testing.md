# Switch to potential

## OPLS-AA classic

* Set charge on all hydrogens to 0.06
* Set charge on terminal Cs to -0.18
* Set charge on mid-chain Cs to -0.12

* Set all dihedral coeffs to original FF
* Set all LJ coeffs to original FF

## OPLS-AA/2020

* Set charge on all hydrogens to 0.06
* Set charge on terminal Cs to -0.18
* Set charge on mid-chain Cs to -0.12

* Set C-C-C-C dihedral coeffs to `0.85 -0.20 0.20 0.0`
* Set H LJ parameters to `2.480 0.026`, terminal Cs to `3.550 0.066`, mid-chain Cs to `3.510 0.066`

## OPLS-AA classic + CM1A

* Set charges from Ligpargen

* Set all dihedral coeffs to original FF
* Set all LJ coeffs to original FF

## OPLS-AA/2020 + CM1A

* Set charges from Ligpargen

* Set C-C-C-C dihedral coeffs to `0.85 -0.20 0.20 0.0`
* Set H LJ parameters to `2.480 0.026`, terminal Cs to `3.550 0.066`, mid-chain Cs to `3.510 0.066`

# Identifying atom and dihedral types

* Hydrogens: atoms with `round(mass) == 1`
* Carbons: atoms with `round(mass) == 12`

* Terminal carbons: carbons with 3 bonds to hydrogens
* Mid-chain carbons: carbons with 2 bonds to hydrogens

# Output file format

```
set type 1 charge -0.18
set type 2 charge -0.12
...
set type 38 charge 0.06


pair_coeff  1 1 0.066 3.5000000
pair_coeff  2 2 0.066 3.5000000
...
pair_coeff 38 38 0.030 2.5000000

bond_coeff ...

dihedral_coeff ...
```
