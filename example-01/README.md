# PURPOSE OF THE EXERCISE: 
## How to calculate and plot molecular orbitals of benzene (actually sign(psi(r))*|psi(r)|^2)
-------------------------------------------------------

**Steps to perform:**

1. `pw.x` SCF calculation as to calculate Kohn-Sham states
```bash
   pw.x < pw.scf.in 2>&1 | tee pw.scf.out
```

2. `pp.x` (post-processing) calculation of all valence and LUMO
   molecular orbitals ( actually $sign(psi(r)) * |psi(r)|^2$ )
```bash
   pp.x < pp.psi2.in 2>&1 | tee pp.psi2.out
```
   the resulting $sign(psi(r)) * |psi(r)|^2$ are written to files
   `psi2.c6h6_K001_B0*.xsf`


3. plot one of generated XSF files with `VESTA, e.g.:
```bash
       VESTA psi2.c6h6_K001_B001.xsf
```

