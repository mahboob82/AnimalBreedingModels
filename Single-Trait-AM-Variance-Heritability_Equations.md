# Question 1. How to calculate variance components and genetic parameters directly via BLUPF90 programs?

# Answer:

## Suppose, I have a simple single trait Animal model with only one additive random effect (additive animal effect only)
  1) Additive effect number was 5 (hint: more hints are generally found in the pedigree file name i.e., renadd05.ped)  
  2) Residual Variance (here it is always R_1_1). 

 
```sh
OPTION se_covar_function Vg G_5_5_1_1
OPTION se_covar_function Vp G_5_5_1_1+R_1_1
OPTION se_covar_function h2 G_5_5_1_1/(G_5_5_1_1+R_1_1)
```
* Warning: Do not put a blank space before or after a particular component.

